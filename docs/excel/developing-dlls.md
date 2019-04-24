---
title: Desenvolver DLLs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- DLLs [excel 2007], criação, criar DLLs [Excel 2007]
ms.assetid: 5d69d06d-a126-4c47-82ad-17112674c8a3
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 89dd7b65ad94ba2fc7e1cf3f99ee163d3003d0fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310917"
---
# <a name="developing-dlls"></a>Desenvolver DLLs

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Uma biblioteca é de uma base de códigos compilados que fornece algumas funcionalidades e dados para um aplicativo executável. As bibliotecas podem ser vinculadas estaticamente ou vinculadas dinamicamente e, convencionalmente, têm extensões de nome de arquivo .lib e .dll, respectivamente. Bibliotecas estáticas (como a biblioteca de tempo de execução C) são vinculadas ao aplicativo na compilação e, portanto, tornam-se parte da resultante executável. O aplicativo carrega uma DLL quando necessário, normalmente quando o aplicativo é iniciado. Um DLL pode carregar e vincular dinamicamente a DLL do outro.
  
## <a name="benefits-of-using-dlls"></a>Benefícios do uso de DLLs

Os principais benefícios de DLLs são os seguintes:
  
- Todos os aplicativos podem compartilhar uma única cópia no disco.
    
- Os arquivos executáveis dos aplicativos são menores.
    
- Eles permitem que grandes projetos de desenvolvimento sejam desmembrados. Desenvolvedores de aplicativo e DLL só precisam concordar uma interface entre suas respectivas partes. Essa interface é exportada pela DLL.
    
- Os desenvolvedores de DLL podem atualizar as DLLs, talvez para torná-las mais eficientes ou para corrigir um bug, sem precisar atualizar todos os aplicativos que as utilizam, desde que a interface exportada da DLL não seja alterada.
    
Você pode usar DLLs para adicionar comandos e funções de planilha no Microsoft Excel.
  
## <a name="resources-for-creating-dlls"></a>Recursos para a criação de DLLs

Para criar uma DLL, você precisa de:
  
- Um editor de código-fonte.
    
- Compilador para ativar o código-fonte do código de objeto que seja compatível com o seu hardware.
    
- Vinculador para adicionar o código de bibliotecas estáticas, quando usado e para criar o arquivo executável DLL.
    
Ambientes de desenvolvimento integrados modernos (IDEs), como o Microsoft Visual Studio, fornecem todas essas coisas. Eles também fornecem muito mais: editores inteligentes, ferramentas para depurar seu código, ferramentas para gerenciar vários projetos, novos assistentes de projeto e muitas outras ferramentas importantes.
  
Você pode criar DLLs em vários idiomas, por exemplo, C++ Pascal e Visual Basic. Dado que o código-fonte da API fornecido com o Excel é C e C ++, somente esses dois idiomas são considerados nesta documentação.
  
## <a name="exporting-functions-and-commands"></a>Exportar comandos e funções

Ao compilar um projeto DLL, o compilador e o vinculador precisam saber quais funções devem ser exportadas para que possam disponibilizá-las para o aplicativo. Esta seção descreve as maneiras de fazer isso.
  
Quando compiladores compilam o código-fonte, em geral, eles alteram os nomes das funções de sua aparência no código-fonte. Eles geralmente fazem isso adicionando o início e/ou final do nome de um processo denominado nome decoração. Você precisa garantir que a função é exportada com um nome reconhecível para o aplicativo ao carregar a DLL. Isso pode significar informar ao vinculador para associar o nome decorado com um nome de exportação mais simples. O nome da exportação pode ser o nome que apareceu originalmente no código-fonte ou qualquer outra coisa.
  
A maneira como o nome é decorado depende do idioma e de como o compilador é instruído a disponibilizar a função, ou seja, a convenção de chamada. A convenção de chamada padrão entre processos para o Windows usada por DLLs é conhecida como a convenção WinAPI. Ele é definida nos arquivos de cabeçalho do Windows como **WINAPI**, que por sua vez é definido usando o **__stdcall** do declarador do Win32.
  
Uma função de exportação de DLL para uso com o Excel (se é uma função de planilha, função equivalente de folha de macro ou comando definido pelo usuário) sempre deve usar a convenção de chamada**WINAPI** / **__stdcall**. É necessário incluir o especificador **WINAPI** explicitamente na definição da função, pois o padrão nos compiladores Win32 é usar a convenção de chamada **__cdecl**, também definida como **WINAPIV**, se nenhuma outra for especificada.
  
Você pode dizer ao vinculador que uma função deve ser exportada, e o nome deve ser conhecido externamente de uma das várias maneiras:
  
- Coloque a função em um arquivo DEF após a palavra-chave **EXPORTS** e defina a configuração do projeto DLL para fazer referência a esse arquivo, vincular. 
    
- Use o declarador **__declspec(dllexport)** na definição de função. 
    
- Use uma diretiva de pré-processador **#pragma** diretiva para enviar o vinculador. 
    
Embora seu projeto possa usar todos os três métodos e seu compilador e vinculador os suportem, você não deve tentar exportar uma função em mais de uma destas maneiras. Por exemplo, suponha que uma DLL contenha dois módulos de código-fonte, um C e um C ++, que contenham duas funções a serem exportadas, **meu\_C\_exportar** e **meu\_Cpp\_exportar** respectivamente. Para simplificar, suponha que cada função receba um único argumento numérico de precisão dupla e retorne o mesmo tipo de dados. As alternativas para exportar cada função usando cada um desses métodos são descritas nas seções a seguir. 
  
### <a name="using-a-def-file"></a>Usando um arquivo DEF

```C
double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

```cpp
double WINAPI my_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

<br/>

O arquivo DEF precisa conter essas linhas.
  
`EXPORTS my_C_export = _my_C_export@8  my_Cpp_export`

<br/>

A sintaxe geral de uma linha que segue uma instrução **EXPORTS** é a seguinte. 
  
`entryname[=internalname] [@ordinal[NONAME]] [DATA] [PRIVATE]`

Observe que a função C foi decorada, mas o arquivo DEF explicitamente força o vinculador a expor a função usando o nome do código-fonte original (neste exemplo). O vinculador exporta implicitamente a função C ++ usando o nome de código original, para que não seja necessário incluir o nome decorado no arquivo DEF.
  
Para chamadas de função da API do Windows de 32 bits, a convenção para a decoração de funções compiladas em C é a seguinte: **function_name** se torna** _ function_name @** _n_ onde _n_ é o número de bytes expressos como um decimal usado por todos os argumentos, com os bytes para cada arredondado para cima até o múltiplo de quatro mais próximo. 
  
> [!NOTE]
> Todos os ponteiros são quatro bytes de largura no Win32. O tipo de retorno não terá impacto sobre o nome da decoração. 
  
É possível forçar o compilador C ++ a expor nomes não-definidos para funções C ++ colocando a função e quaisquer protótipos de função dentro de um "C" externo {…} bloqueio, como é mostrado neste exemplo. (As chaves ** {} ** foram omitidos aqui porque a declaração refere-se somente ao bloco de código de função que o segue imediatamente). 
  
```cpp
extern "C"
double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}

```

Quando você está colocando protótipos de função C em arquivos de cabeçalho que podem ser incluídos em arquivos de origem C ou C ++, inclua a seguinte diretiva de pré-processador.
  
```cpp
#ifdef __cplusplus
extern "C" {
#endif
double WINAPI my_C_export(double x);
double WINAPI my_Cdecorated_Cpp_export(double x);
#ifdef __cplusplus
}
#endif
```

### <a name="using-the-declspecdllexport-declarator"></a>Usando declarador __declspec(dllexport)

A palavra-chave **__declspec(dllexport)** pode ser usada na declaração de função da seguinte maneira. 
  
```cpp
__declspec(dllexport) double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

A palavra-chave **__declspec(dllexport)** deve ser adicionada à esquerda da declaração. As vantagens dessa abordagem são que a função não precisa ser listada em um arquivo DEF e que o status de exportação está correto com a definição. 
  
Se você quiser evitar que uma função C ++ seja disponibilizada com a decoração do nome C ++, você deve declarar a função da seguinte maneira.
  
```cpp
extern "C"
__declspec(dllexport) double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

O vinculador disponibilizará a função como my_undecorated_Cpp_export, ou seja, o nome como aparece no código-fonte sem decoração.
  
### <a name="using-a-pragma-preprocessor-linker-directive"></a>Usando uma diretiva de vinculador de pré-processador #pragma

Versões recentes do Microsoft Visual Studio suportam duas macros predefinidas que, quando usadas em conjunto com uma diretiva **#pragma**, permite que você instrua o vinculador a exportar a função diretamente de dentro do código de função. As macros são __FUNCTION__ e __FUNCDNAME__ (observe o sublinhado duplo em cada extremidade) que são expandidas para os nomes das funções não decoradas e decoradas, respectivamente. 
  
Por exemplo, quando você está usando o Microsoft Visual Studio, essas linhas podem ser incorporadas em um arquivo de cabeçalho comum da seguinte maneira.
  
```cpp
#if _MSC_VER > 1200 // Later than Visual Studio 6.0
#define EXPORT comment(linker, "/EXPORT:"__FUNCTION__"="__FUNCDNAME__)
#else // Cannot use this way of exporting functions.
#define EXPORT
#endif // else need to use DEF file or __declspec(dllexport)

```

Se esse cabeçalho estiver incluído nos arquivos de origem, as duas funções de exemplo poderão ser exportadas da seguinte maneira.
  
Código C:
  
```C
double WINAPI my_C_export(double x)
{
#pragma EXPORT
/* Modify x and return it. */
    return x * 2.0;
}
```

Código C++:
  
```cpp
double WINAPI my_Cpp_export(double x)
{
#pragma EXPORT
// Modify x and return it.
    return x * 2.0;
}
```

Observe que a diretiva deve ser colocada no corpo da função e só está expandida quando nenhuma das opções do compilador **/EP** ou **/p** é definida. Essa técnica elimina a necessidade de um arquivo DEF ou declaração **__declspec(dllexport)** e mantém a especificação do seu status de exportação com o código de função. 
  
## <a name="see-also"></a>Confira também

- [Acessar DLLs no Excel](how-to-access-dlls-in-excel.md)
- [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md)
- [Conceitos de programação do Excel](excel-programming-concepts.md)
- [Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)

