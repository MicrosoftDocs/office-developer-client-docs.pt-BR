---
title: Desenvolver DLLs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- DLLs [excel 2007], a criação, criando DLLs [Excel 2007]
localization_priority: Normal
ms.assetid: 5d69d06d-a126-4c47-82ad-17112674c8a3
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 030cdd4358d9a71841eca6acfcef6e71839e02a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765284"
---
# <a name="developing-dlls"></a>Desenvolver DLLs

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Uma biblioteca é um corpo de código compilado que fornece algumas funcionalidades e os dados para um aplicativo executável. Bibliotecas podem ser vinculadas estaticamente ou dinamicamente vinculadas e convencionalmente têm o. lib extensões de nome de arquivo e. dll respectivamente. Bibliotecas estáticas (por exemplo, a biblioteca de tempo de execução do C) são vinculadas ao aplicativo na compilação e então se torna parte do executável resultante. O aplicativo carrega uma DLL quando ela for necessária, geralmente quando o aplicativo é iniciado. Uma DLL pode carregar e vincular dinamicamente a outro DLL.
  
## <a name="benefits-of-using-dlls"></a>Benefícios do uso de DLLs

Os principais benefícios do DLLs são:
  
- Todos os aplicativos podem compartilhar uma única cópia no disco.
    
- Arquivos executáveis de nos aplicativos são mantidos menores.
    
- Eles permitem que os projetos de desenvolvimento de grandes sejam divididos. Os desenvolvedores de aplicativos e DLL precisam concorda apenas uma interface entre seus respectivos papéis. Esta interface é exportada pela DLL.
    
- Os desenvolvedores DLL podem atualizar DLLs — talvez para torná-los mais eficiente ou para corrigir um bug — sem precisar atualizar todos os aplicativos que usá-lo, desde que a interface exportada da DLL não é alterado.
    
Você pode usar DLLs para adicionar funções de planilha e comandos no Microsoft Excel.
  
## <a name="resources-for-creating-dlls"></a>Recursos para a criação de DLLs

Para criar uma DLL, você precisará dos seguintes itens:
  
- Um editor de código fonte.
    
- Um compilador para transformar o código-fonte em código do objeto que é compatível com o seu hardware.
    
- Um vinculador para adicionar o código de bibliotecas estáticas, onde usado e para criar o arquivo DLL executável.
    
Ambientes de desenvolvimento integrado moderno (IDEs), como o Microsoft Visual Studio, fornecem todas essas coisas. Eles também fornecem uma excelente oportunidade mais: inteligente de editores, ferramentas para depurar seu código, ferramentas para gerenciar vários projetos, novos assistentes de projeto e muitas outras ferramentas importantes.
  
Você pode criar DLLs em diversos idiomas, por exemplo, C/C++, Pascal e Visual Basic. Considerando que o código-fonte API fornecido com o Excel é C e C++, apenas esses dois idiomas são considerados nesta documentação.
  
## <a name="exporting-functions-and-commands"></a>Exportando funções e comandos

Ao compilar um projeto DLL, o compilador e vinculador precisam saber quais funções são a ser exportado para que eles podem torná-los disponíveis para o aplicativo. Esta seção descreve as maneiras como isso pode ser feito.
  
Quando compiladores compilar código-fonte, em geral, eles alteram os nomes das funções de sua aparência no código-fonte. Eles geralmente fazem isso por meio da adição de início e/ou final do nome, em um processo conhecido como simplificação de nome. Você deve certificar-se de que a função é exportada com um nome reconhecível para o aplicativo ao carregar a DLL. Isso pode significar informando o vinculador para associar o nome decorado com um nome de exportação mais simples. O nome da exportação pode ser o nome como ele apareceu originalmente no código-fonte ou outra coisa.
  
A maneira como o nome é decorado depende do idioma e como o compilador é instruído para disponibilizar a função, ou seja, a convenção de chamada. A convenção de chamada de standard entre processos para Windows usado pelo DLLs é conhecida como a convenção WinAPI. Ele é definido em arquivos de cabeçalho do Windows como **WINAPI**, que é definido por sua vez usando o declarador do Win32 **__stdcall**.
  
Uma função de exportação de DLL para uso com o Excel (se é uma função de planilha, folha de macro de função equivalente ou comando definida pelo usuário) sempre deve usar o **WINAPI** / **__stdcall** convenção de chamada. É necessário incluir o especificador **WINAPI** explicitamente na definição da função como o padrão no Win32 compiladores é usar o **cdecl** chamar convenção, também são definida como **WINAPIV**, se nenhuma estiver especificada.
  
Você pode dizer o vinculador que uma função deve ser exportado e o nome é conhecido por externamente de várias maneiras:
  
- Coloque a função em um arquivo DEF após a palavra-chave **exportações** e defina sua configuração de projeto DLL para fazer referência a este arquivo quando vincular. 
    
- Use o declarador **__declspec(dllexport)** na definição da função. 
    
- Use uma diretiva de pré-processador **#pragma** para enviar uma mensagem para o vinculador. 
    
Embora o seu projeto pode usar todos os três métodos e seu compilador e vinculador oferecer suporte a eles, você não deve tentar uma função em mais de uma dessas maneiras de exportação. Por exemplo, suponha que uma DLL contém módulos de código fonte dois, um C e um C++, que contêm as duas funções a serem exportados, **Meu\_C\_exportar** e **minha\_Cpp\_exportar** respectivamente. Para manter a simplicidade, suponha que cada função usa um único argumento numérico de precisão dupla e retorna o mesmo tipo de dados. As alternativas para a exportação de cada função usando cada um desses métodos são descritas nas seções a seguir. 
  
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

A sintaxe geral de uma linha que segue uma instrução **exportações** é da seguinte maneira. 
  
`entryname[=internalname] [@ordinal[NONAME]] [DATA] [PRIVATE]`

Observe que a função C foi decorada, mas o arquivo DEF explicitamente força o vinculador expor a função usando o nome de código fonte original (neste exemplo). O vinculador implicitamente exporta a função C++ utilizando o nome de código original, para que ele não é necessário incluir o nome decorado no arquivo DEF.
  
Para chamadas de função de API do Windows de 32 bits, a convenção para a decoração de funções compilado C é da seguinte maneira: **nome_da_função** se torna _ **nome_da_função @** _n_ onde _n_ é o número de bytes, expressado como um número decimal ocupado por todos os argumentos, com os bytes para cada arredondado para cima até o múltiplo mais próximo de quatro. 
  
> [!NOTE]
> Todos os ponteiros são ampla no Win32 de quatro bytes. O tipo de retorno tem nenhum impacto sobre simplificação de nome. 
  
É possível forçar o compilador C++ expor nomes não decorados para funções C++ colocando-se a função e protótipos de função, dentro de um externo "C" {...} bloquear, conforme mostrado neste exemplo. (Das chaves **{}** forem omitidos aqui porque a declaração refere-se apenas para o bloco de código de função que o segue imediatamente). 
  
```cpp
extern "C"
double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}

```

Quando você está colocando C protótipos de função nos arquivos de cabeçalho que poderiam ser incluídos nos arquivos de origem do C ou C++, você deve incluir a diretiva de pré-processador a seguir.
  
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

### <a name="using-the-declspecdllexport-declarator"></a>Usando o declarador __declspec(dllexport)

A palavra-chave **__declspec(dllexport)** pode ser usada na declaração de função da seguinte maneira. 
  
```cpp
__declspec(dllexport) double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

A palavra-chave **__declspec(dllexport)** deve ser adicionada à extrema esquerda da declaração. As vantagens dessa abordagem são que a função não precisa ser listadas em um arquivo de definição e o status de exportação é correta com a definição. 
  
Se você deseja evitar uma função C++ sendo disponibilizada com a simplificação de nome de C++, você deve declarar a função da seguinte maneira.
  
```cpp
extern "C"
__declspec(dllexport) double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

O vinculador disponibilizarão a função como my_undecorated_Cpp_export, ou seja, o nome como ele aparece no código-fonte com sem decoração.
  
### <a name="using-a-pragma-preprocessor-linker-directive"></a>Usar uma diretiva de pré-processador vinculador #pragma

Versões recentes do Microsoft Visual Studio oferecem suporte a duas macros predefinidas que, quando usado em conjunto com uma diretiva **#pragma** , permitem que você instruir o vinculador para exportar a função diretamente de dentro do código de função. As macros são __função__ e __FUNCDNAME__ (Observe o sublinhado duplo em cada extremidade) que são expandidos para os nomes de função não decorado e decorada respectivamente. 
  
Por exemplo, quando você estiver usando o Microsoft Visual Studio, essas linhas podem ser incorporadas em um arquivo de cabeçalho comuns da seguinte maneira.
  
```cpp
#if _MSC_VER > 1200 // Later than Visual Studio 6.0
#define EXPORT comment(linker, "/EXPORT:"__FUNCTION__"="__FUNCDNAME__)
#else // Cannot use this way of exporting functions.
#define EXPORT
#endif // else need to use DEF file or __declspec(dllexport)

```

Se este conector está incluído nos arquivos de origem, as funções de dois exemplo podem ser exportadas da seguinte maneira.
  
Código de C:
  
```C
double WINAPI my_C_export(double x)
{
#pragma EXPORT
/* Modify x and return it. */
    return x * 2.0;
}
```

Código de C++:
  
```cpp
double WINAPI my_Cpp_export(double x)
{
#pragma EXPORT
// Modify x and return it.
    return x * 2.0;
}
```

Observe que a diretiva deve ser colocada dentro do corpo da função e é expandida apenas quando nenhuma das opções de compilador **/EP** ou **/P** é definido. Essa técnica remove a necessidade de um arquivo DEF, ou declaração de **__declspec(dllexport)** e mantém a especificação de seu status de exportação com o código de função. 
  
## <a name="see-also"></a>Confira também

- [Acessar DLLs no Excel](how-to-access-dlls-in-excel.md)
- [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md)
- [Excel Programming Concepts](excel-programming-concepts.md)
- [Desenvolvimento de XLLs do Excel](developing-excel-xlls.md)

