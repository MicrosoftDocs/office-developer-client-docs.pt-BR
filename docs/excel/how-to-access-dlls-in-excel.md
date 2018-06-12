---
title: Acesso DLLs no Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- accessing dlls [excel 2007],DLLs [Excel 2007], accessing in Excel
localization_priority: Normal
ms.assetid: e2bfd6ea-efa3-45c1-a5b8-2ccb8650c6ab
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: bfb562b6bbe824124c6b5a691745d076720ee004
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765376"
---
# <a name="access-dlls-in-excel"></a>Acesso DLLs no Excel

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Voc� pode acessar uma fun��o ou um comando DLL no Microsoft Excel de diversas maneiras:
  
- Por meio de um m�dulo de c�digo do Microsoft Visual Basic for Applications (VBA) no qual a fun��o ou o comando foi disponibilizado usando uma instru��o **Declare**. 
    
- Por meio de uma folha de macro XLM usando as fun��es **CALL** ou **REGISTER**. 
    
- Diretamente da planilha ou de um item personalizado na interface do usu�rio (IU).
    
Esta documenta��o n�o aborda as fun��es XLM. � recomend�vel que voc� use uma das duas outras abordagens.
  
Para ser acessada diretamente da planilha ou de um item personalizado na IU, primeiro a fun��o ou o comando dever�o ser registrados no Excel. Para saber mais sobre o registro de comandos e de fun��es, consulte [Accessing XLL Code in Excel](accessing-xll-code-in-excel.md).
  
## <a name="calling-dll-functions-and-commands-from-vba"></a>Chamando funções DLL e comandos do VBA

Voc� pode acessar fun��es e comandos DLL no VBA usando a instru��o **Declare**. Essa instru��o tem uma sintaxe para os comandos e outra para as fun��es. 
  
- **Sintaxe 1 � comandos**
    
  ```vb
  [Public | Private] Declare Sub name Lib "libname" [Alias "aliasname"] [([arglist])]
  ```

- **Sintaxe 2 � fun��es**
    
  ```vb
  [Public | Private] Declare Function name Lib "libname" [Alias "aliasname"] [([arglist])] [As type]
  ```

As palavras-chave **Public** e **Private** especificam o escopo da fun��o importada: o projeto inteiro do Visual Basic ou apenas o m�dulo do Visual Basic, respectivamente. O nome � o que voc� deseja usar no c�digo VBA. Se ele for diferente do nome na DLL, ser� necess�rio usar o especificador "nomedoalias" do Alias e nomear a fun��o como exportada pela DLL. Se voc� quiser acessar uma fun��o de DLL por refer�ncia a um n�mero ordinal de DLL, dever� fornecer um nome de alias, que � o ordinal com o prefixo **#**.
  
Os comandos devem retornar **void**. As fun��es devem retornar tipos que o VBA possa reconhecer **ByVal**. Isso significa que alguns tipos s�o retornados com mais facilidade pela modifica��o dos argumentos existentes: cadeias de caracteres, matrizes, tipos definidos pelo usu�rio e objetos.
  
> [!NOTE]
> [!OBSERVA��O] O VBA n�o pode verificar se a lista de argumentos e os estados retornados no m�dulo do Visual Basic s�o iguais aos codificados na DLL. Verifique isso com muito cuidado, pois um erro pode causar uma falha no Excel. 
  
Quando os argumentos da fun��o ou do comando n�o forem passados por refer�ncia ou por ponteiro, dever�o ser precedidos pela palavra-chave **ByVal** na declara��o **arglist**. Quando uma fun��o C/C++ obtiver argumentos do ponteiro, ou quando uma fun��o C++ obtiver argumentos de refer�ncia, dever�o ser passados **ByRef**. A palavra-chave **ByRef** pode ser omitida das listas de argumentos porque � o padr�o no VBA. 
  
### <a name="argument-types-in-cc-and-vba"></a>Tipos de argumento em C/C++ e VBA

Voc� deve observar o seguinte ao comparar as declara��es de tipos de argumento no C/C++ e no VBA.
  
- Uma **String** do VBA � passada como um ponteiro para uma estrutura BSTR byte-cadeia de caracteres quando passada ByVal e como um ponteiro para um ponteiro quando passada **ByRef**.
    
- Uma **Variant** do VBA que cont�m uma cadeia de caracteres � passada como um ponteiro para uma cadeia de caracteres de caractere largo Unicode usando a estrutura BSTR quando passada **ByVal** e como um ponteiro para um ponteiro quando passada **ByRef**.
    
- O **Integer** do VBA � um equivalente do tipo de 16 bits para um signed short no C/C++. 
    
- O **Long** do VBA � um tipo de 32 bits equivalente a um signed int no C/C++. 
    
- O VBA e o C/C++ permitem a defini��o de tipos de dados definidos pelo usu�rio usando as instru��es **Type** e **struct**, respectivamente. 
    
- O VBA e o C/C++ d�o suporte ao tipo de dados **Variant**, definido para o C/C++ nos arquivos de cabe�alho do OLE/COM do Windows como VARIANT. 
    
- As matrizes do VBA s�o **SafeArrays** OLE, definidos para o C/C++ no arquivo de cabe�alho OLE/COM do Windows como **SAFEARRAY**.
    
- O tipo de dados **Currency** do VBA � passado como uma estrutura do tipo **CY**, definida no arquivo de cabe�alho wtypes.h do Windows, quando passado **ByVal**, e como um ponteiro para ponteiro para isso quando passado **ByRef**.
    
No VBA, os elementos de dados em tipos de dados definidos pelo usu�rio s�o empacotados em limites de 4 bytes, enquanto que, no Visual Studio, por padr�o, eles s�o empacotados em limites de 8 bytes. Portanto, você deve colocar a definição da estrutura de C/C++ em um `#pragma pack(4) … #pragma pack()` bloco para evitar elementos sendo fora de alinhamento. 
  
A seguir, um exemplo de defini��es de tipo de usu�rio equivalentes.
  
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

O VBA d� suporte a uma s�rie de valores maior em alguns casos ao que o Excel consegue dar suporte. O double do VBA � compat�vel com IEEE, dando suporte a n�meros subnormais atualmente arredondados para baixo para zero na planilha. O tipo **Date** do VBA pode representar datas desde 1-Jan-0100 usando datas serializadas negativas. O Excel s� permite datas serializadas maiores ou iguais a zero. O tipo **Currency** do VBA � um inteiro de 64 bits dimensionado � pode obter precis�o sem suporte em doubles de 8 bytes e, portanto, n�o tem correspond�ncia na planilha. 
  
O Excel s� passa Variants dos tipos a seguir para uma fun��o definida pelo usu�rio do VBA.
  
|**Tipo de dados do VBA**|**Sinalizadores de bit do tipo Variant do C/C++**|**Descri��o**|
|:-----|:-----|:-----|
|Double  <br/> |**VT_R8** <br/> ||
|Booliano  <br/> |**VT_BOOL** <br/> ||
|Data  <br/> |**VT_DATE** <br/> ||
|String  <br/> |**VT_BSTR** <br/> |Cadeia de caracteres de byte Bstr OLE  <br/> |
|Intervalo  <br/> |**VT_DISPATCH** <br/> |Refer�ncias de intervalo e de c�lula  <br/> |
|Variant com uma matriz  <br/> |**VT_ARRAY** | **VT_VARIANT** <br/> |Matrizes literais  <br/> |
|Ccy  <br/> |**VT_CY** <br/> |Inteiro de 64 bits dimensionado para permitir quatro casas decimais de precis�o.  <br/> |
|Variant com erro  <br/> |**VT_ERROR** <br/> ||
||**VT_EMPTY** <br/> |C�lulas vazias ou argumentos omitidos  <br/> |
   
Voc� pode verificar o tipo de uma Variant passado no VBA usando o **VarType**, exceto que a fun��o retorna o tipo dos valores do intervalo quando chamado com refer�ncias. Para determinar se uma **Variant** � um objeto de refer�ncia **Range**, voc� poder� usar a fun��o **IsObject**. 
  
Voc� pode criar **Variants** com matrizes de variantes no VBA de um **Range** ao atribuir sua propriedade **Value** a uma **Variant**. Todas as c�lulas no intervalo de origem formatadas como a moeda padr�o para as configura��es regionais em vigor no momento ser�o convertidas em elementos da matriz do tipo **Currency**. Todas as c�lulas formatadas como datas ser�o convertidas em elementos de matriz do tipo **Date**. As c�lulas com cadeias de caracteres ser�o convertidas em Variants **BSTR** de caractere longo. As c�lulas com erros ser�o convertidas em **Variants** do tipo **VT_ERROR**. As c�lulas com **Boolean** **True** ou **False** ser�o convertidas em **Variants** do tipo **VT_BOOL**. 
  
> [!NOTE]
> [!OBSERVA��O] A **Variant** armazena **True** como �1 e **False** como 0. Os n�meros n�o s�o formatados como datas ou valores monet�rios s�o convertidos em Variants do tipo **VT_R8**. 
  
### <a name="variant-and-string-arguments"></a>Argumentos Variant e a cadeia de caracteres

O Excel funciona internamente com cadeias de caracteres Unicode de caractere longo. Quando uma fun��o definida pelo usu�rio do VBA � declarada como obtendo um argumento de **String**, o Excel converte a cadeia de caracteres fornecida em uma cadeia de caracteres de byte de uma forma espec�fica da localidade. Se voc� quiser que uma cadeia de caracteres Unicode seja passada para sua fun��o, sua fun��o definida pelo usu�rio do VBA dever� aceitar um argumento de **Variant** em vez de um de **String**. Sua fun��o DLL poder� ent�o aceitar a cadeia de caracteres de caractere longo BSTR **Variant** do VBA. 
  
Para retornar cadeias de caracteres Unicode para o VBA de uma DLL, modifique um argumento de cadeia de caracteres **Variant** no local. Para que isso funcione, voc� dever� declarar a fun��o DLL como obtendo um ponteiro para a **Variant** em seu c�digo C/C++ e declarar o argumento no c�digo VBA como  `ByRef varg As Variant`. A mem�ria da cadeia de caracteres antiga dever� ser liberada e o valor da nova cadeia de caracteres criado usando o OLE. A cadeia de caracteres Bstr s� funciona na DLL.
  
Para retornar uma cadeia de caracteres de byte para o VBA de uma DLL, voc� dever� modificar um argumento BSTR de cadeia de caracteres de byte existente. Para que isso funcione, voc� dever� declarar a fun��o DLL como obtendo um ponteiro para um ponteiro para o BSTR e em seu c�digo C/C++ e declarar o argumento no c�digo VBA como " **ByRef varg As String**".
  
Voc� s� deve manipular as cadeias de caracteres passadas dessas maneiras do VBA usando as fun��es de cadeia de caracteres BSTR OLE para evitar problemas relacionados � mem�ria. Por exemplo, ser� necess�rio chamar **SysFreeString** para liberar a mem�ria antes de substituir o que foi passado na cadeia de caracteres e **SysAllocStringByteLen** ou **SysAllocStringLen** para alocar espa�o para uma nova cadeia de caracteres. 
  
Voc� pode criar erros de planilha do Excel como **Variants** no VBA usando a fun��o **CVerr** com argumentos como os mostrados na tabela a seguir. Os erros de planilha tamb�m pode ser retornados para o VBA de uma DLL usando **Variants** do tipo **VT_ERROR** e com os valores a seguir no campo **ulVal**. 
  
|**Erro**|**Valor da Variant ulVal**|**Argumento CVerr**|
|:-----|:-----|:-----|
|#NULL!  <br/> |2148141008  <br/> |2000  <br/> |
|#DIV/0!  <br/> |2148141015  <br/> |2007  <br/> |
|#VALUE!  <br/> |2148141023  <br/> |2015  <br/> |
|#REF!  <br/> |2148141031  <br/> |2023  <br/> |
|#NAME?  <br/> |2148141037  <br/> |2029  <br/> |
|#NUM!  <br/> |2148141044  <br/> |2036  <br/> |
|#N/A  <br/> |2148141050  <br/> |2042  <br/> |
   
Observe que o valor da Variant **ulVal** dado � equivalente ao valor do argumento de **CVerr** mais x800A0000 hexadecimal. 
  
## <a name="calling-dll-functions-directly-from-the-worksheet"></a>Chamando funções DLL diretamente a partir de planilha

Voc� n�o pode acessar fun��es DLL Win32 da planilha sem, por exemplo, usar o VBA ou o XLM como interfaces ou sem permitir que o Excel conhe�a a fun��o, seus argumentos e seu tipo de retorno com anteced�ncia. O processo de fazer isso se chama registro.
  
As maneiras nas quais as fun��es de uma DLL podem ser acessadas na planilha s�o as seguintes:
  
- Declare a fun��o no VBA como descrito anteriormente e acesse-a por meio de uma fun��o definida pelo usu�rio do VBA.
    
- Chame a fun��o DLL usando CALL em uma folha de macro XLM ou acesse-a por meio de uma fun��o definida pelo usu�rio XLM.
    
- Use um comando XLM ou VBA para chamar a fun��o **REGISTER** XLM, que fornece as informa��es de que o Excel precisa para reconhecer a fun��o quando ela for inserida em uma c�lula de planilha. 
    
- Transforme a DLL em um XLL e registre a fun��o usando a fun��o **xlfRegister** da API do C quando o XLL for ativado. 
    
A quarta abordagem � autocontida: o c�digo que registra as fun��es e o c�digo da fun��o est�o contidos no mesmo projeto de c�digo. Fazer altera��es no suplemento n�o envolve fazer altera��es em uma planilha XLM ou em um m�dulo de c�digo VBA. Para fazer isso de uma maneira bem gerenciada mantendo-se no limite dos recursos da API do C, voc� dever� transformar sua DLL em um XLL e carregar o suplemento resultante usando o Gerenciador de Suplementos. Isso permite que o Excel chame uma fun��o exposta por sua DLL quando o suplemento � carregado ou ativado, a partir do qual voc� poder� registrar todas as fun��es contidas em seu XLL e realizar a inicializa��o de qualquer outra DLL.
  
## <a name="calling-dll-commands-directly-from-excel"></a>Chamar comandos DLL diretamente do Excel

Os comandos de DLL Win32 n�o podem ser diretamente acessados de caixas de di�logo e de menus do Excel sem que haja uma interface, como o VBA, ou sem o registro pr�vio dos comandos.
  
As maneiras nas quais voc� pode acessar os comandos de uma DLL s�o as seguintes:
  
- Declare o comando no VBA como descrito anteriormente e acesse-o por meio de uma macro do VBA.
    
- Chame o comando da DLL usando **CALL** em uma folha de macros XLM e acesse-o por meio de uma macro XLM. 
    
- Use um comando XLM ou VBA para chamar a fun��o **REGISTER** XLM, que fornece as informa��es de que o Excel precisa para reconhecer o comando quando ele for inserido em uma caixa de di�logo que espere o nome de um comando de macro. 
    
- Transforme a DLL em um XLL e registre o comando usando a fun��o **xlfRegister** da API do C. 
    
Como discutido anteriormente no contexto de fun��es de DLL, a quarta abordagem � a mais autocontida, mantendo o c�digo de registro pr�ximo ao c�digo do comando. Para fazer isso, voc� deve transformar sua DLL em um XLL e carregar o suplemento resultante usando o Gerenciador de Suplementos. O registro de comandos dessa maneira tamb�m permite que voc� anexe o comando a um elemento da interface do usu�rio, como um menu personalizado ou configure uma intercepta��o de evento que chame o comando em um determinado pressionamento de tecla ou outro evento.
  
Todos os comandos de XLL registrados no Excel s�o considerados pelo Excel como do formato a seguir.
  
```cpp
int WINAPI my_xll_cmd(void)
{
// Function code...
    return 1;
}
```

> [!NOTE]
> [!OBSERVA��O] O Excel ignorar� o valor de retorno, a menos que ele seja chamado de uma folha de macros XLM; nesse caso, o valor de retorno ser� convertido em **TRUE** ou em **FALSE**. Dessa forma, voc� dever� retornar 1 se o seu comando tiver sido executado com �xito e 0 caso ele tenha falhado ou tenha sido cancelado pelo usu�rio. 
  
## <a name="dll-memory-and-multiple-dll-instances"></a>DLL de memória e várias instâncias DLL

Quando um aplicativo carrega uma DLL, o c�digo execut�vel da DLL � carregado na pilha global de forma que possa ser executado, e � alocado um espa�o na pilha global para suas estruturas de dados. O Windows usa o mapeamento de mem�ria para fazer com que essas �reas da mem�ria apare�am como se estivessem no processo do aplicativo, de forma que o aplicativo possa acess�-las.
  
Se um segundo aplicativo carregar a DLL, o Windows n�o far� outra c�pia do c�digo execut�vel da DLL, j� que a mem�ria � somente leitura. O Windows mapeia a mem�ria do c�digo execut�vel da DLL para os processos de ambos os aplicativos. No entanto, ele aloca um segundo espa�o para uma c�pia privada das estruturas de dados da DLL e mapeia essa c�pia apenas para o segundo processo. Isso garante que os aplicativos n�o interfiram nos dados de DLL um do outro.
  
Isso significa que os desenvolvedores n�o precisa se preocupar com a possibilidade de as vari�veis est�ticas e globais e as estruturas de dados serem acessados por mais de um aplicativo, ou por mais de uma inst�ncia do mesmo aplicativo. Todas as inst�ncias de todos os aplicativos obt�m sua pr�pria c�pia dos dados da DLL.
  
Os desenvolvedores de DLL n�o precisam se preocupar com o fato de a mesma inst�ncia do aplicativo chamar sua DLL v�rias vezes de threads diferentes, porque isso pode resultar em conten��o dos dados da inst�ncia. Para saber mais, consulte [Memory Management in Excel](memory-management-in-excel.md).
  
## <a name="see-also"></a>Ver tamb�m

- [Developing DLLs](developing-dlls.md) 
- [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md)

