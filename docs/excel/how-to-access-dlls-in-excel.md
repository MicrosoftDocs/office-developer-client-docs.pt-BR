---
title: Acessar DLLs no Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- acessar dlls [excel 2007], DLLs [Excel 2007], acessar no Excel
localization_priority: Normal
ms.assetid: e2bfd6ea-efa3-45c1-a5b8-2ccb8650c6ab
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bfb562b6bbe824124c6b5a691745d076720ee004
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765376"
---
# <a name="access-dlls-in-excel"></a>Acessar DLLs no Excel

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Você pode acessar um comando ou função DLL no Microsoft Excel de diversas maneiras:
  
- Por meio de um módulo de código Microsoft VBA (Visual Basic for Applications) na qual a função ou comando foi disponibilizada usando uma instrução **Declare**. 
    
- Por meio de uma folha de macro XLM usando as funções **CALL** ou **REGISTER**. 
    
- Diretamente da planilha ou de um item personalizado na IU (interface do usuário).
    
Esta documentação não aborda as funções XLM. É recomendável que você use uma das outras duas abordagens.
  
Para acessar diretamente na planilha ou em um item personalizado na interface de usuário, primeiro a função ou o comando deve ser registrado no Excel. Confira mais informações sobre como registrar os comandos e as funções, veja [Acessar código XLL no Excel](accessing-xll-code-in-excel.md).
  
## <a name="calling-dll-functions-and-commands-from-vba"></a>Chamar funções e comandos DLL do VBA

Você pode acessar os comandos e as funções DLL do VBA usando a instrução **Declare**. Essa instrução tem uma sintaxe para comandos e uma para funções. 
  
- **Sintaxe 1 – comandos**
    
  ```vb
  [Public | Private] Declare Sub name Lib "libname" [Alias "aliasname"] [([arglist])]
  ```

- **Sintaxe 2 – funções**
    
  ```vb
  [Public | Private] Declare Function name Lib "libname" [Alias "aliasname"] [([arglist])] [As type]
  ```

As palavras-chave opcionais **Public** e **Private** especificam o escopo da função importada: todo o projeto do Visual Basic ou apenas o módulo do Visual Basic, respectivamente. O nome é aquele que você deseja usar no código VBA. Se for diferente do nome da DLL, você deve usar o especificador de Alias "nomedoalias" e deve fornecer o nome da função como exportado pela DLL. Se quiser acessar uma função DLL por referência para um número ordinal de DLL, você deve fornecer um nome de alias, que é o ordinal precedido por **#**.
  
Os comandos devem retornar **void**. As funções devem retornar tipos que o VBA pode reconhecer **ByVal**. Isso significa que alguns tipos são retornados com maior facilidade ao modificar os argumentos no lugar: cadeias de caracteres, matrizes, objetos e tipos definidos pelo usuário.
  
> [!NOTE]
> O VBA não pode verificar se a lista de argumentos e o retorno declarado no módulo do Visual Basic são os mesmos codificados na DLL. Você deve verificar isso sozinho com muito cuidado, pois um erro pode causar uma falha no Excel. 
  
Quando os argumentos do comando ou da função não são passados por ponteiro ou referência, devem ser precedidos pela palavra-chave **ByVal** com a declaração **arglist**. Quando uma função C/C++ tem os argumentos de ponteiro ou quando uma função C++ tem os argumentos de referência, eles deveriam passar por **ByRef**. A palavra-chave **ByRef** pode ser omitida das listas de argumentos porque é o padrão no VBA. 
  
### <a name="argument-types-in-cc-and-vba"></a>Tipos de argumento no C/C++ e no VBA

Você deve observar o seguinte ao comparar as declarações dos tipos de argumentos no C/C++ e VBA.
  
- Uma **String** do VBA é passada como um ponteiro para uma estrutura BSTR de cadeia de caracteres de bytes quando houver passado por ByVal e como um ponteiro para um ponteiro quando passada por **ByRef**.
    
- Uma **Variant** do VBA que contém uma cadeia de caracteres é passada como um ponteiro para uma estrutura BSTR de cadeia de caracteres largos Unicode quando passada por **ByVal** e como um ponteiro para um ponteiro quando passada por **ByRef**.
    
- O **Integer** do VBA é um tipo de 16 bits equivalente a um curto assinado no C/C++. 
    
- O **Long** do VBA é um tipo de 32 bits equivalente a um curto assinado no C/C++. 
    
- O VBA e o C++ permitem a definição de tipos de dados definidos pelo usuário, usando respectivamente as instruções **Type** e **struct**. 
    
- O VBA e o C++ oferecem suporte ao tipo de dados **Variant**, definido para o C++ nos arquivos de cabeçalho Windows OLE/COM, como VARIANT. 
    
- As matrizes do VBA são **SafeArrays** OLE, definidas para o C++ nos arquivos de cabeçalho Windows OLE/COM, como **SAFEARRAY**.
    
- O tipo de dados **Currency** do VBA é passado como uma estrutura de tipo **CY**, definido no arquivo de cabeçalho de Windows wtypes.h, quando passado por **ByVal** e como um ponteiro para isso quando passado por **ByRef**.
    
No VBA, os elementos de dados nos tipos de dados definidos pelo usuário são compactados nos limites de 4 bytes, enquanto no Visual Studio, por padrão, eles são compactados nos limites de 8 bytes. Dessa forma, você deve inserir a definição de estrutura do C/C++ em um bloco `#pragma pack(4) … #pragma pack()` para evitar erros de alinhamento de elementos. 
  
A seguir, um exemplo de definições de tipo de usuário equivalentes.
  
```vb
Type VB_User_Type
    i As Integer
    d As Double
    s As String
End Type

```

```cpp
#pragma pack(4)
struct C_user_type
{
    short iVal;
    double dVal;
    BSTR bstr; // VBA String type is a byte string
}
#pragma pack() // restore default

```

Em alguns casos, o VBA dá suporte a um intervalo maior de valores do que o Excel. O VBA duplo é compatível com IEEE e dá suporte a números subnormais que atualmente são arredondados para zero na planilha. O tipo **Date** do VBA pode representar datas a partir de 1-Jan-0100 usando datas serializadas negativas. O Excel permite somente datas serializadas maiores ou iguais a zero. O tipo **Date** do VBA, um número inteiro de 64 bits em escala, pode alcançar uma precisão que não tem suporte em 8 bytes duplos e, portanto, não tem correspondência na planilha. 
  
O Excel somente passa Variants dos seguintes tipos para uma função definida pelo usuário do VBA.
  
|**Tipo de dados do VBA**|**Sinalizadores de bit do tipo Variant do C/C++**|**Descrição**|
|:-----|:-----|:-----|
|Duplo  <br/> |**VT_R8** <br/> ||
|Boolean  <br/> |**VT_BOOL** <br/> ||
|Data  <br/> |**VT_DATE** <br/> ||
|Cadeia de caracteres  <br/> |**VT_BSTR** <br/> |Cadeia de caracteres de byte Bstr OLE  <br/> |
|Intervalo  <br/> |**VT_DISPATCH** <br/> |Referências de intervalos e células  <br/> |
|Variant com uma matriz  <br/> |**VT_ARRAY** | **VT_VARIANT** <br/> |Matrizes literais  <br/> |
|Ccy  <br/> |**VT_CY** <br/> |Número inteiro de 64 bits dimensionado para permitir 4 casas decimais de precisão.  <br/> |
|Variant com erro  <br/> |**VT_ERROR** <br/> ||
||**VT_EMPTY** <br/> |Argumentos omitidos ou células vazias  <br/> |
   
Você pode verificar o tipo de uma Variant passada no VBA usando o **VarType**, com a exceção que a função retorna o tipo dos valores de intervalo quando chamado com referências. Para determinar se um **Variant** é um objeto **Range** de referência, você pode usar a função **IsObject**. 
  
Você pode criar **Variants** que contêm matrizes de variantes do VBA de um **Range** atribuindo suas propriedades **Value** para uma **Variant**. Todas as células no intervalo de origem que são formatadas usando o formato de moeda padrão das configurações regionais em vigor no momento são convertidas em elementos de matriz do tipo **Currency**. Todas as células formatadas como datas são convertidas em elementos de matriz do tipo **Date**. As células que contêm cadeias de caracteres são convertidas em Variants **BSTR** de caracteres largos. As células que contêm erros são convertidas em **Variants** do tipo **VT_ERROR**. As células contendo **Boolean** **True** ou **False** são convertidas em **Variants** do tipo **VT_BOOL**. 
  
> [!NOTE]
> A **Variant** armazena **True** como -1 e **False** como 0. Os números não formatados, como datas ou valores de moedas, são convertidos em Variants do tipo **VT_R8**. 
  
### <a name="variant-and-string-arguments"></a>Argumentos de variant ou de cadeia de caracteres

O Excel funciona internamente com cadeias de caracteres Unicode de caracteres largos. Quando se declara que uma função definida pelo usuário do VBA obtém um argumento **String**, o Excel converte a cadeia de caracteres fornecida em uma cadeia de caracteres de bytes em forma específica do local. Se quiser que a função seja passada em uma cadeia de caracteres Unicode, a função definida pelo usuário do VBA deve aceitar um argumento **Variant**, em vez de um **String**. A função DLL pode aceitar aquela **Variant** da cadeia de caracteres larga de BSTR do VBA. 
  
Para retornar cadeias de caracteres Unicode de uma DLL para o VBA, você deve modificar um argumento de cadeia de caracteres **Variant** no local. Para fazer isto, declare a função DLL como fazendo um ponteiro para a **Variant** e no seu código C/C++, e declare o argumento no código VBA como `ByRef varg As Variant`. A memória da cadeia de caracteres antiga deve ser liberada e o novo valor da cadeia de caracteres deve ser criado usando a as funções de cadeia de caracteres OLE Bstr somente na DLL.
  
Para retornar uma cadeia de caracteres de bytes em VBA de uma DLL, você deve modificar um argumento BSTR da cadeia de caracteres de bytes no local. Para fazer isto, você deve declarar a função DLL como fazendo um ponteiro para um ponteiro para o BSTR e no seu código C/C++, e declarar o argumentos no código VBA como ' **ByRef varg As String**'.
  
Você só deve manusear as cadeias de caracteres que são passadas dessa maneira do VBA usando as funções de cadeia de caracteres BSTR OLE para evitar problemas de memória. Por exemplo, você deverá chamar **SysFreeString** para liberar a memória antes de sobrescrever a cadeia de caracteres passada, e **SysAllocStringByteLen** ou **SysAllocStringLen** para alocar espaço para uma nova cadeia de caracteres. 
  
Você pode criar erros de planilha do Excel como **Variants** em VBA usando a função **CVerr** com argumentos, como mostrado na tabela a seguir. Os erros de planilha também podem ser retornados em VBA para uma DLL que usa **Variants** do tipo **VT_ERROR** e com os seguintes valores no campo **ulVal**. 
  
|**Erro**|**Valor da Variant ulVal**|**Argumento CVerr**|
|:-----|:-----|:-----|
|#NULL!  <br/> |2148141008  <br/> |2000  <br/> |
|#DIV/0!  <br/> |2148141015  <br/> |2007  <br/> |
|#VALUE!  <br/> |2148141023  <br/> |2015  <br/> |
|#REF!  <br/> |2148141031  <br/> |2023  <br/> |
|#NAME?  <br/> |2148141037  <br/> |2029  <br/> |
|#NUM!  <br/> |2148141044  <br/> |2036  <br/> |
|#N/A  <br/> |2148141050  <br/> |2042  <br/> |
   
Observe que o valor fornecido de Variant **ulVal** é equivalente ao valor do argumento **CVerr** mais o hexadecimal x800A0000. 
  
## <a name="calling-dll-functions-directly-from-the-worksheet"></a>Como chamar funções DLL diretamente da planilha

Não é possível acessar as funções Win32 DLL da planilha sem, por exemplo, usar o VBA ou XLM como interfaces, ou sem informar o Excel com antecedência sobre o tipo de função, seus argumentos e o tipo de retorno. Esse processo é chamado de registro.
  
Veja a seguir as maneiras para acessar as funções de uma DLL na planilha:
  
- Declare a função em VBA, como descrito anteriormente, e acesse-a por meio de uma função VBA definida pelo usuário.
    
- Chame a função DLL usando CALL em uma planilha de macro XLM e acesse-a por uma função XLM definida pelo usuário.
    
- Use um comando XLM ou VBA para chamar a função XLM **REGISTER**, que fornece as informações que o Excel precisa para reconhecer a função quando ela é inserida em uma célula da planilha. 
    
- Transforme a DLL em um XLL e registre a função usando a função API de C **xlfRegister** quando o XLL estiver ativado. 
    
A quarta abordagem é autocontida: o código que registra as funções e o código da função estão contidos no mesmo projeto de código. Fazer alterações no suplemento não inclui fazer alterações em uma planilha XLM ou em um módulo de código do VBA. Para fazer isso de maneira bem gerenciada enquanto permanece dentro dos recursos da API de C, é necessário transformar a DLL em um XLL e carregar o suplemento resultante usando o Gerenciador de Suplemento, o que permite que o Excel chame uma função exposta pelo seu DLL quando o suplemento é carregado ou ativado, na qual você pode registrar todas as funções contidas na sua XLL e executar qualquer outra inicialização de DLL.
  
## <a name="calling-dll-commands-directly-from-excel"></a>Chamando comandos de DLL diretamente do Excel

Os comandos Win32 DLL não são acessíveis diretamente nos menus e caixas de diálogo do Excel sem a existência de uma interface, como o VBA, ou sem os comandos serem registrados com antecedência.
  
Estas são as maneiras para acessar os comandos de uma DLL:
  
- Declare o comando no VBA como descrito anteriormente e acesse-o por meio de uma macro do VBA.
    
- Chame o comando da DLL usando **CALL** em uma folha de macros XLM e acesse-o por meio de uma macro XLM. 
    
- Use um comando XLM ou VBA para chamar a função de XLM **REGISTER**, que fornece as informações que o Excel precisa para reconhecer o comando quando ele é inserido na caixa de diálogo que espera o nome de um comando de macro. 
    
- Transforme a DLL em XLL e registre o comando usando a função API de C **xlfRegister**. 
    
Como discutido anteriormente no contexto das funções DLL, a quarta abordagem é a mais autocontida, mantendo o código de registro parecido com o código de comando. Para isso, você deve transformar a DLL em um XLL e carregar o suplemento resultante usando o Gerenciador de Suplemento. Registrar os comandos dessa maneira também permite anexar o comando a um elemento da interface do usuário, como um menu personalizado, ou configurar um ajuste de registro de evento que chama o comando em um determinado pressionamento de tecla ou outro evento.
  
Todos os comandos do XLL registrados com o Excel são considerados pelo Excel da forma a seguir.
  
```cpp
int WINAPI my_xll_cmd(void)
{
// Function code...
    return 1;
}
```

> [!NOTE]
> O Excel ignora o valor de retorno, a menos que ele seja chamado de uma planilha de macro XLM; neste caso, o valor de retorno é convertido para **TRUE** ou **FALSE**. Portanto, você deve retornar 1 se o comando foi executado com sucesso e 0 se falhou ou foi cancelado pelo usuário. 
  
## <a name="dll-memory-and-multiple-dll-instances"></a>Memória de DLL e várias instâncias de DLL

Quando um aplicativo carrega uma DLL, o código executável da DLL é carregado na pilha global para que possa ser executado e o espaço é alocado na pilha global das suas estruturas de dados. O Windows usa o mapeamento de memória para fazer com que essas áreas de memória apareçam como se estivessem no processo do aplicativo para que o aplicativo possa acessá-las.
  
Se um segundo aplicativo em seguida carrega a DLL, o Windows não faz outra cópia do código executável de DLL, pois essa memória é somente leitura. O Windows mapeia a memória de códigos executáveis DLL para os processos dos dois aplicativos, mas aloca um segundo espaço para uma cópia particular das estruturas de dados da DLL e mapeia esta cópia ao segundo processo. Isso garante que nenhum aplicativo possa interferir nos dados de DLL dos outros.
  
Ou seja, os desenvolvedores DLL não precisam se preocupar com as variáveis globais e estáticas, e as estruturas de dados acessadas por mais de um aplicativo ou mais de uma instância do mesmo aplicativo. Todas as instâncias de todos os aplicativos obtêm sua própria cópia dos dados da DLL.
  
Os desenvolvedores de DLL precisam se preocupar com a mesma instância de um aplicativo chamando sua DLL várias vezes de threads diferentes, porque isso pode resultar em contenção dos dados dessa instância. Para saber mais, confira [Gerenciamento de memória no Excel](memory-management-in-excel.md).
  
## <a name="see-also"></a>Confira também

- [Desenvolver DLLs](developing-dlls.md) 
- [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md)

