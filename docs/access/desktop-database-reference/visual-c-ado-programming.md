---
title: Programação do ADO do Visual C++
TOCTitle: Visual C++ ADO Programming
ms:assetid: 117c4fad-8c11-5e3a-ea0c-18811e87475f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248878(v=office.15)
ms:contentKeyID: 48543319
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 55e4bf1476112cc950b72e8bfd1659226704f991
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25890005"
---
# <a name="visual-c-ado-programming"></a>Programação do ADO do Visual C++


**Aplica-se a**: Access 2013, o Office 2013

A Referência à API do ADO descreve a funcionalidade da API (Application Programming Interface, Interface de Programação de Aplicativos) utilizando uma sintaxe semelhante ao Microsoft Visual Basic. Embora o público-alvo esteja todos os usuários, programadores ADO empregam diversos idiomas, como o Visual Basic, Visual C++ (com e sem o ** \#importar** diretiva) e Visual J++ (com o pacote de classe ADO/WFC).

Para acomodar essa diversidade, os [Índices de sintaxe do ADO para Visual C++](using-ado-with-microsoft-visual-c.md) fornecem sintaxe específica da linguagem Visual C++ com links para descrições comuns de funcionalidade, parâmetros, comportamentos excepcionais e assim por diante, na Referência à API.

O ADO é implementado com as interfaces COM (Component Object Model). Entretanto, é mais fácil para os programadores trabalhar com o COM em certas linguagens de programação do que em outras. Por exemplo, quase todos os detalhes da utilização do COM são tratados de forma implícita para os programadores do Visual Basic, enquanto os programadores do Visual C++ devem eles mesmos se ater a esses detalhes.

As seções a seguir resumem os detalhes para programadores C e C++ usando o ADO e o ** \#importar** diretiva. Ela se concentra em tipos de dados específicos do COM (**Variant**, **BSTR**e **SafeArray**) e tratamento de erros (\_com\_erro).

## <a name="using-the-import-compiler-directive"></a>Usando o \#importar a diretiva de compilador

O ** \#importar** diretiva de compilador do Visual C++ simplifica o trabalho com as propriedades e métodos do ADO. A diretiva tem o nome de um arquivo contendo uma biblioteca de tipo, como ADO .dll (Msado15.dll), e gera arquivos de cabeçalho contendo declarações typedef, ponteiros inteligentes para interfaces e constantes enumeradas. Cada interface é encapsulada, ou agrupada, em uma classe.

Para cada operação dentro de uma classe (isto é, uma chamada de método ou propriedade), há uma declaração para chamar a operação diretamente (isto é, o formato "bruto" da operação) e uma declaração para chamar a operação bruta e lançar um erro COM, se a operação não é executada com sucesso. Se a operação for uma propriedade, haverá uma diretiva de compilador que cria uma sintaxe alternativa para a operação que tem uma sintaxe como a de Visual Basic.

Operações que recuperar o valor de uma propriedade têm nomes do formulário, **obter * * * propriedade*. Operações que defina o valor de uma propriedade têm nomes do formulário, **colocar * * * propriedade*. Operações que defina o valor de uma propriedade com um ponteiro para um objeto ADO têm nomes do formulário, **PutRef * * * propriedade*.

Você pode obter ou definir uma propriedade chamando estes formatos:

```vb 
 
variable = objectPtr->GetProperty(); // get property value 
objectPtr->PutProperty(value); // set property value 
objectPtr->PutRefProperty(&value); // set property with object pointer 
```

## <a name="using-property-directives"></a>Utilizando diretivas de propriedade

O ** \_ \_declspec(property...)** diretiva de compilador é uma extensão de idioma específico do Microsoft C declara uma função usada como uma propriedade para ter uma sintaxe alternativa. Consequentemente, você pode definir ou obter valores de uma propriedade de modo semelhante ao Visual Basic. Por exemplo, é possível definir e obter uma propriedade desta forma:

```vb 
 
objectPtr->property = value; // set property value 
variable = objectPtr->property; // get property value 
```

Observe que não é necessário codificar:

```vb 
 
objectPtr->PutProperty(value); // set property value 
variable = objectPtr->GetProperty; // get property value 
```

O compilador irá gerar apropriada **Get * * *-*, **Coloque**-, ou **PutRef * * * propriedade* chamada com base na sintaxe alternativa declarada e se a propriedade está sendo lidos ou gravados.

O ** \_ \_declspec(property...)** diretiva de compilador só pode declarar **obter**, **colocar**ou **obtêm** ou **colocam** sintaxe alternativa para uma função. As operações somente-leitura têm uma declaração **get**; as operações somente-gravação têm apenas uma declaração **put**; as operações de leitura e gravação têm as declarações **get** e **put**.

Apenas duas declarações são possíveis com essa diretiva; No entanto, cada propriedade pode ter três funções de propriedade: **obter * * * propriedade*, **colocar * * * propriedade*, e **PutRef * * * propriedade*. Nesse caso, somente dois formatos de propriedade têm uma sintaxe alternativa.

Por exemplo, o propriedade **ActiveConnection** do objeto **Command** é declarado como uma sintaxe alternativa para **obter * * * ActiveConnection* e **PutRef * * * ActiveConnection*. O **PutRef**- sintaxe é uma boa opção porque prática, será conveniente colocar um objeto de **Conexão** (ou seja, um indicador de objeto de **Conexão** ) aberto nessa propriedade normalmente. Por outro lado, o objeto **Recordset** tem **Get**-, **Coloque**-, e **PutRef * * * ActiveConnection* operações, mas nenhuma sintaxe alternativa.

## <a name="collections-the-getitem-method-and-the-item-property"></a>Coleções, o método GetItem e a propriedade Item

O ADO define várias coleções, incluindo **Fields**, **Parameters**, **Properties** e **Errors**. No Visual C++, o método **GetItem(***index***)** retorna um membro da coleção. *Index* é uma **Variant**, o valor que é um índice numérico do membro na coleção ou uma sequência de caracteres contendo o nome do membro.

O ** \_ \_declspec(property...)** diretiva de compilador declara a propriedade **Item** como uma sintaxe alternativa ao método de **obter GetItem ()** fundamental da cada coleção. A sintaxe alternativa usa colchetes e se assemelha à referência de matriz. Em geral, os dois formatos se assemelham a:

```vb
    collectionPtr->GetItem(index); 
    collectionPtr->Item[index]; 
```

Por exemplo, atribua um valor a um campo de um objeto **Recordset** , chamado ***rs***, derivado da tabela **authors** de banco de dados **pubs** . Use a propriedade de **item ()** para acessar o terceiro **campo** do objeto **Recordset** a coleção **Fields** (coleções são indexadas a partir de zero; assume o terceiro campo é chamado ***au\_fname***). Em seguida, chame o método **Value()** no objeto **Field** para atribuir um valor de sequência de caracteres.

Isso pode ser expressado no Visual Basic das quatro formas a seguir (as últimas duas são exclusivas para Visual Basic; outras linguagem não têm equivalentes):

```vb 
 
rs.Fields.Item(2).Value = "value" 
rs.Fields.Item("au_fname").Value = "value" 
rs(2) = "value" 
rs!au_fname = "value" 
```

O equivalente no Visual C++ para a primeira das duas formas acima é:

```cpp 
 
rs->Fields->GetItem(long(2))->PutValue("value"); 
rs->Fields->GetItem("au_fname")->PutValue("value"); 
```

\-ou -(a sintaxe alternativa para a propriedade **Value** também é mostrada)

```cpp 
 
rs->Fields->Item[long(2)]->Value = "value"; 
rs->Fields->Item["au_fname"]->Value = "value"; 
```

## <a name="com-specific-data-types"></a>Tipos de dados específicos do COM

Em geral, qualquer tipo de dados do Visual Basic encontrado na Referência à API do ADO tem um equivalente no Visual C++. Isso inclui tipos de dados padrão, como **unsigned char** para Visual Basic **Byte**, **short** para **Integer** e **long** para **Long**. Consulte os Índices de sintaxe para ver exatamente o que é exigido para operadores de um determinado método ou propriedade.

As exceções a essa regra são os tipos de dados específicos para COM: **Variant**, **BSTR** e **SafeArray**.

## <a name="variant"></a>Variant

Uma **Variant** é um tipo de dados estruturado que contém um membro de valor e um membro de tipo de dados. Uma **Variant** pode conter uma ampla quantidade de outros tipos de dados, incluindo outra Variant, BSTR, Boolean, IDispatch ou ponteiro IUnknown, moeda, data etc. O COM também fornece métodos que facilitam a conversão de um tipo de dados para outro.

O ** \_variant\_t** classe encapsula e gerencia o tipo de dados **Variant** .

Quando a referência de API do ADO informa que um método ou propriedade tem um valor, isso normalmente significa que o valor é transmitido em uma ** \_variant\_t**.

Essa regra é explicitamente verdadeira quando a seção **Parâmetros** nos tópicos da Referência à API do ADO informa que um operador é uma **Variant**. Uma exceção é quando a documentação explicitamente informa que o operador tem um tipo de dados padrão, como **Long** ou **Byte** ou uma enumeração. Outra exceção é quando o operador tem uma **String**.

## <a name="bstr"></a>BSTR

Um **BSTR** (**B**asic **STR**ing) é um tipo de dados estruturado que contém uma sequência de caracteres e seu comprimento. O COM fornece métodos para alocar, manipular e liberar **BSTR**.

O ** \_bstr\_t** classe encapsula e gerencia o tipo de dados **BSTR** .

Quando a referência de API do ADO informa que um método ou uma propriedade tem um valor **String** , isso significa que o valor é na forma de um ** \_bstr\_t**.

## <a name="casting-variantt-and-bstrt-classes"></a>Lançar \_variant\_t e \_bstr\_Classes t

Geralmente não é necessário ao código explicitamente um ** \_variant\_t** ou ** \_bstr\_t** em um argumento para uma operação. Se o ** \_variant\_t** ou ** \_bstr\_t** classe tem um construtor que corresponda ao tipo de dados do argumento, em seguida, o compilador irá gerar apropriada ** \_variant\_t** ou ** \_ BSTR\_t**.

Entretanto, se o argumento for ambíguo, isto é, o tipo de dados do argumento for correspondente a mais de um construtor, será necessário orientar o argumento com o tipo de dados apropriado para chamar o construtor correto.

Por exemplo, a declaração para o método **Recordset::Open** é:

```vb 
 
 HRESULT Open ( 
 const _variant_t & Source, 
 const _variant_t & ActiveConnection, 
 enum CursorTypeEnum CursorType, 
 enum LockTypeEnum LockType, 
 long Options ); 
```

O argumento ActiveConnection utiliza uma referência para um ** \_variant\_t**, que você pode código como uma cadeia de caracteres de conexão ou um ponteiro para um objeto de **Conexão** aberto.

O correto ** \_variant\_t** será construída implicitamente se você passar uma cadeia de caracteres, como "DSN = pubs; uid = sa; pwd =;", ou um ponteiro como "(IDispatch \*) pConn".

Ou você pode codificar explicitamente um ** \_variant\_t** contendo um ponteiro como "\_variant\_t ((IDispatch \*) pConn, true)". A projeção, (IDispatch \*), resolva a ambiguidade com outro construtor que usa um ponteiro para uma interface IUnknown.

Um ponto importante a ser mencionado é que o ADO é uma interface IDispatch. Sempre que um ponteiro para um objeto do ADO for transmitido como uma **Variant**, aquele ponteiro deve ser orientado como um ponteiro para uma interface IDispatch.

O último caso explicitamente codes o segundo argumento boolean do construtor com seu valor padrão opcional, true. Este argumento faz com que o construtor de **Variant** chamar seu método de () **AddRef**, que indica de ADO automaticamente chamar o ** \_variant\_t::Release**método () quando terminar a chamada de método ou uma propriedade do ADO.

## <a name="safearray"></a>SafeArray

**SafeArray** é um tipo de dados estruturado que contém uma matriz de outros tipos de dados. Um **SafeArray** é chamado *seguros* porque ele contém informações sobre os limites de cada dimensão de matriz e limita o acesso aos elementos de matriz dentro desses limites.

Quando a Referência à API do ADO informa que um método ou uma propriedade tem ou retorna uma matriz, isso significa que o método ou a propriedade tem ou retorna **SafeArray**, não uma matriz C/C++ nativa.

Por exemplo, o segundo parâmetro do método **OpenSchema** do objeto **Connection** requer uma matriz de valores **Variant**. Esses valores **Variant** devem ser transmitidos como elementos de **SafeArray**, e esse **SafeArray** deve ser definido como o valor de outra **Variant**. Isso significa que outra **Variant** é transmitida como o segundo argumento de **OpenSchema**.

Como exemplos adicionais, o primeiro argumento do método **Find** é uma **Variant** cujo valor é um **SafeArray** com uma dimensão; cada um dos argumentos principal e secundário opcionais de **AddNew** é um **SafeArray** com uma dimensão; e o valor de retorno do método **GetRows** é uma **Variant** cujo valor é um **SafeArray** com duas dimensões.

## <a name="missing-and-default-parameters"></a>Parâmetros Missing e Default

O Visual Basic permite parâmetros Missing nos métodos. Por exemplo, o método **Open** do objeto **Recordset** tem cinco parâmetros, mas você pode ignorar os parâmetros intermediários e excluir os parâmetros à direita. Um **BSTR** ou **Variant** padrão será substituído dependendo do tipo de dados do operador ausente.

Em C/C++, todos os operadores devem ser especificados. Se você deseja especificar um parâmetro missing cujo tipo de dados é uma cadeia de caracteres, especifique um ** \_bstr\_t** que contém uma cadeia de caracteres nula. Se você deseja especificar um parâmetro missing cujo tipo de dados é um **Variant**, especifique um ** \_variant\_t** com um valor de DISP\_f\_PARAMNOTFOUND e um tipo de VT\_erro. Como alternativa, especifique o equivalente ** \_variant\_t** constante, **vtMissing**, que é fornecido pelo ** \#importar** diretiva.

Três métodos são exceções ao uso típico de **vtMissing**. Eles são os métodos **Execute** dos objetos **Connection** e **Command**, e os métodos **NextRecordset** do objeto **Recordset**. A seguir estão suas assinaturas:

```vb 
 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcnnexecute_HV10294345.xml( _bstr_t CommandText, VARIANT * RecordsAffected, 
 long Options ); // Connection 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthcmdexecute_HV10294344.xml( VARIANT * RecordsAffected, VARIANT * Parameters, 
 long Options ); // Command 
_RecordsetPtr Invalid DDUE based on source, error:link not allowed in code, link filename:mdmthnextrec_HV10294541.xml( VARIANT * RecordsAffected ); // Recordset 
```

Os parâmetros *RecordsAffected* e *Parameters* são ponteiros para uma **Variant**. *Parameters* é um parâmetro de entrada que especifica o endereço de uma **Variant** contendo um único parâmetro, ou uma matriz de parâmetros, que modifica o comando que está sendo executado. *RecordsAffected* é um parâmetro de saída que especifica o endereço de uma **Variant**, em que o número de linhas afetadas pelo método é retornado.

No objeto **Command** método **Execute** , indicar que nenhuma parâmetros forem especificados, definindo *parâmetros* para uma \&vtMissing (que é recomendado) ou para o ponteiro nulo (ou seja, **Nulo** ou zero (0)). Se o *parâmetro* for definido como o ponteiro nulo, o método internamente substituirá o equivalente do **vtMissing**e conclui a operação.

Em todos os métodos, indica que o número de registros afetados não deve ser retornado, definindo *RecordsAffected* para o ponteiro nulo. Nesse caso, o ponteiro nulo não é mais um parâmetro Missing nem sequer uma indicação de que o método deve descartar o número de registros afetados.

Dessa forma, para esses três métodos, é válido codificar algo como:

```vb 
 
pConnection->Execute("commandText", NULL, adCmdText); 
pCommand->Execute(NULL, NULL, adCmdText); 
pRecordset->NextRecordset(NULL); 
```

## <a name="error-handling"></a>Tratamento de erros

Em COM, a maioria das operações retorna um código HRESULT que indica se uma função foi concluída com êxito. O ** \#importar** diretiva gera um código de wrapper ao redor de cada propriedade ou método "raw" e verifica o HRESULT retornado. Se o HRESULT indica uma falha, o código de wrapper lança um erro COM chamando \_com\_problema\_errorex() com o HRESULT retornar código como um argumento. Os objetos de erro do COM podem ser capturados em um bloco **try**-**catch**. (Para a mesma da eficiência, catch uma referência a um ** \_com\_erro** objeto.)

Lembre-se, esses são os erros do ADO: eles resultam de falha em operações do ADO. Os erros retornados pelo provedor subjacente aparecem como objetos **Error** na coleção **Errors** do objeto **Connection**.

O ** \#importar** diretiva cria apenas erro rotinas de tratamento de métodos e propriedades declaradas na ADO. dll. Contudo, você pode aproveitar esse mesmo mecanismo de tratamento de erros escrevendo sua própria macro de verificação de erros ou sua função inline. Consulte o tópico [Extensões do Visual C++](visual-c-extensions-for-ado.md) ou o código nas seções a seguir para obter exemplos.

## <a name="visual-c-equivalents-of-visual-basic-conventions"></a>Equivalentes do Visual C++ de convenções do Visual Basic

A seguir está um resumo de várias convenções na documentação do ADO, codificadas no Visual Basic, bem como seus equivalentes no Visual C++.

## <a name="declaring-an-ado-object"></a>Declarando um objeto do ADO

No Visual Basic, uma variável de objeto do ADO (nesse caso para um objeto **Recordset** ) é declarada como se segue:

```vb 
 
Dim rst As ADODB.Recordset 
```

A cláusula, "ADODB. Recordset", é o ProgID do objeto **Recordset** , conforme definido no registro. Uma nova instância de um objeto **Record** é declarado como a seguir:

```vb 
 
Dim rst As New ADODB.Recordset 
```

\-ou -

```vb 
 
Dim rst As ADODB.Recordset 
Set rst = New ADODB.Recordset 
```

No Visual C++, o ** \#importar** diretiva gera declarações de tipo de ponteiro inteligente para todos os objetos do ADO. Por exemplo, uma variável que aponta para um ** \_Recordset** objeto é do tipo ** \_RecordsetPtr**e é declarada como se segue:

```cpp 
 
_RecordsetPtr rs; 
```

Uma variável que aponta para uma nova instância de um ** \_Recordset** objeto é declarado como se segue:

```cpp 
 
_RecordsetPtr rs("ADODB.Recordset"); 
```

\-ou -

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance("ADODB.Recordset"); 
```

\-ou -

```cpp 
 
_RecordsetPtr rs; 
rs.CreateInstance(__uuidof(_Recordset)); 
```

Depois que o método **CreateInstance** é chamado, a variável pode ser utilizada como se segue:

```cpp 
 
rs->Open(...); 
```

Observe que, em um caso, o "." operador é usado como se a variável fosse uma instância de uma classe (rs. CreateInstance) e em outro caso, o "-\>" operador é usado como se a variável fosse um ponteiro para uma interface (rs -\>Open).

Uma variável pode ser usada de duas maneiras, porque o "-\>" operador está sobrecarregado para permitir que uma instância de uma classe para que atue como um ponteiro para uma interface. Um membro da classe privada da variável instância contém um ponteiro para o ** \_Recordset** interface; o "-\>" operador retorna desse ponteiro; e o ponteiro retornado acessa os membros a ** \_Recordset** objeto.

## <a name="coding-a-missing-parameter"></a>Codificando um parâmetro Missing

Quando é necessário codificar um operador **String** ausente no Visual Basic, você simplesmente omite o operador. Você deve especificar o operador no Visual C++. Código um ** \_bstr\_t** que tem uma sequência vazia como um valor.

```cpp 
 
_bstr_t strMissing(L""); 
```

## <a name="coding-a-missing-parameter"></a>Codificando um parâmetro Missing

Quando é necessário codificar um operador **Variant** ausente no Visual Basic, você simplesmente omite o operador. Você deve especificar todos os operadores no Visual C++. Código um parâmetro **Variant** missing com um ** \_variant\_t** definido como o valor especial, DISP\_f\_PARAMNOTFOUND e tipo, VT\_erro. Como alternativa, especificar **vtMissing**, que é equivalente a uma constante pré-definidos fornecidos pelo ** \#importar** diretiva.

```cpp 
 
_variant_t vtMissingYours(DISP_E_PARAMNOTFOUND, VT_ERROR); 
```

\-ou uso-

```cpp 
 
...vtMissing...; 
```

## <a name="declaring-a-variant"></a>Declarando uma Variant

No Visual Basic, uma **Variant** é declarada como a instrução **Dim** como se segue:

```vb 
 
Dim VariableName As Variant 
```

No Visual C++, declare uma variável como tipo ** \_variant\_t**. Alguns esquemático ** \_variant\_t** declarações são mostradas abaixo.


> [!NOTE]
> <P>[!OBSERVAçãO] Essas declarações fornecem uma pequena ideia do que você codificaria em seu próprio programa. Para obter mais informações, consulte os exemplos abaixo e a documentação do Visual C++.</P>



```cpp 
 
_variant_t VariableName(value); 
_variant_t VariableName((data type cast) value); 
_variant_t VariableName(value, VT_DATATYPE); 
_variant_t VariableName(interface * value, bool fAddRef = true); 
```

## <a name="using-arrays-of-variants"></a>Utilizando matrizes de Variants

No Visual Basic, as matrizes de **Variants** podem ser codificadas com a instrução **Dim** ou podem utilizar a função **Array**, como demonstrado no seguinte código de exemplo:

```vb 
 
Public Sub ArrayOfVariants 
Dim cn As ADODB.Connection 
Dim rs As ADODB.Recordset 
Dim fld As ADODB.Field 
 
cn.Open "DSN=pubs", "sa", "" 
rs = cn.OpenSchema(adSchemaColumns, _ 
 Array(Empty, Empty, "authors", Empty)) 
For Each fld in rs.Fields 
 Debug.Print "Name = "; fld.Name 
Next fld 
rs.Close 
cn.Close 
End Sub 
```

O exemplo a seguir do Visual C++ demonstra o uso de **SafeArray** utilizado com um ** \_variant\_t**.


> [!NOTE]
> <P>[!OBSERVAçãO] As seguintes notas correspondem às seções comentadas no exemplo de código.</P>



1.  Novamente, a função inline TESTHR() é definida para aproveitar a existência do mecanismo de tratamento de erros.

2.  Você precisa apenas de uma matriz com uma dimensão para poder utilizar **SafeArrayCreateVector**, em vez da declaração **SAFEARRAYBOUND** e da função **SafeArrayCreate** de objetivos gerais. A seguir está um exemplo de como o código é, usando **SafeArrayCreate**:
    
    ```cpp 
     
     SAFEARRAYBOUND sabound[1]; 
     sabound[0].lLbound = 0; 
     sabound[0].cElements = 4; 
     pSa = SafeArrayCreate(VT_VARIANT, 1, sabound); 
    ```

3.  O esquema identificado pela constante enumerada, **adSchemaColumns**, é associado a quatro colunas de restrição: tabela\_catálogo, tabela\_esquema, tabela\_nome e a coluna\_nome. Portanto, uma matriz de valores **Variant** com quatro elementos é criada. Em seguida, um valor de restrição que corresponde à tabela, a terceira coluna\_nome, for especificado. O **Recordset** retornado consiste em várias colunas, um subconjunto de colunas de restrição. Os valores das colunas de restrição para cada linha retornada deve ser igual aos valores de restrição correspondentes.

4.  Aqueles que estão familiarizados com **SafeArrays** podem-se que **SafeArrayDestroy**(de) não é chamado antes de sair. Na verdade, chamar () de **SafeArrayDestroy**neste caso fará com que uma exceção de tempo de execução. O motivo é que o destrutor para vtCriteria chamará () de **VariantClear**quando o ** \_variant\_t** sai do escopo, qual liberará **SafeArray**. Chamar **SafeArrayDestroy**, sem limpando manualmente o ** \_variant\_t**, causaria o destrutor tentar limpar um ponteiro **SafeArray** inválido. Se **SafeArrayDestroy** for chamado, o código será parecido com:
    
    ```cpp 
     
     TESTHR(SafeArrayDestroy(pSa)); 
     vtCriteria.vt = VT_EMPTY; 
     vtCriteria.parray = NULL; 
    ```
    
    No entanto, é muito mais simples permitir que o ** \_variant\_t** gerencie **SafeArray**.

<!-- end list -->

```cpp 
 
#import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
#include <stdio.h> 
 
// Note 1 
inline void TESTHR( HRESULT _hr ) 
 { if FAILED(_hr) _com_issue_error(_hr); } 
 
void main(void) 
{ 
 CoInitialize(NULL); 
 try 
 { 
 _RecordsetPtr pRs("ADODB.Recordset"); 
 _ConnectionPtr pCn("ADODB.Connection"); 
 _variant_t vtTableName("authors"), 
 vtCriteria; 
 long ix[1]; 
 SAFEARRAY *pSa = NULL; 
 
 pCn->Open("DSN=pubs;User ID=MyUserId;pwd=MyPassword;Provider=MSDASQL;", "", "", 
 adConnectUnspecified); 
// Note 2, Note 3 
 pSa = SafeArrayCreateVector(VT_VARIANT, 1, 4); 
 if (!pSa) _com_issue_error(E_OUTOFMEMORY); 
 
// Specify TABLE_NAME in the third array element (index of 2). 
 
 ix[0] = 2; 
 TESTHR(SafeArrayPutElement(pSa, ix, &vtTableName)); 
 
// There is no Variant constructor for a SafeArray, so manually set the 
// type (SafeArray of Variant) and value (pointer to a SafeArray). 
 
 vtCriteria.vt = VT_ARRAY | VT_VARIANT; 
 vtCriteria.parray = pSa; 
 
 pRs = pCn->OpenSchema(adSchemaColumns, vtCriteria, vtMissing); 
 
 long limit = pRs->GetFields()->Count; 
 for (long x = 0; x < limit; x++) 
 printf("%d: %s\n", x+1, 
 ((char*) pRs->GetFields()->Item[x]->Name)); 
// Note 4 
 pRs->Close(); 
 pCn->Close(); 
 } 
 catch (_com_error &e) 
 { 
 printf("Error:\n"); 
 printf("Code = %08lx\n", e.Error()); 
 printf("Code meaning = %s\n", (char*) e.ErrorMessage()); 
 printf("Source = %s\n", (char*) e.Source()); 
 printf("Description = %s\n", (char*) e.Description()); 
 } 
 CoUninitialize(); 
} 
```

## <a name="using-property-getputputref"></a>Utilizando as propriedades Get/Put/PutRef

No Visual Basic, o nome de uma propriedade não é qualificado se ela for recuperada, atribuída ou atribuída a uma referência.

```vb
    Public Sub GetPutPutRef 
    Dim rs As New ADODB.Recordset 
    Dim cn As New ADODB.Connection 
    Dim sz as Integer 
    cn.Open "Provider=sqloledb;Data Source=yourserver;" & _ 
     "Initial Catalog=pubs;Integrated Security=SSPI;" 
    rs.PageSize = 10 
    sz = rs.PageSize 
    rs.ActiveConnection = cn 
    rs.Open "authors",,adOpenStatic 
    ' ... 
    rs.Close 
    cn.Close 
    End Sub
```

Este exemplo do Visual C++ demonstra **Get**/**colocar**/**PutRef * * * propriedade*.


> [!NOTE]
> <P>[!OBSERVAçãO] As seguintes notas correspondem às seções comentadas no exemplo de código.</P>



1.  Este exemplo usa duas formas de um argumento de cadeia de caracteres ausente: uma constante explícita, **strMissing**e uma cadeia de caracteres que o compilador irá usar para criar um temporário ** \_bstr\_t** que continuará a existir para o escopo do método **Open** .

2.  Não é necessário orientar o operador de rs -\>Putrefactiveconnection para (IDispatch \*) porque o tipo do operador já é (IDispatch \*).
    
    ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr cn("ADODB.Connection"); 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _bstr_t strMissing(L""); 
     long oldPgSz = 0, 
     newPgSz = 5; 
     
    // Note 1 
     cn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     strMissing, "", 
     adConnectUnspecified); 
     
     oldPgSz = rs->GetPageSize(); 
     // -or- 
     oldPgSz = rs->PageSize; 
     
     rs->PutPageSize(newPgSz); 
     // -or- 
     rs->PageSize = newPgSz; 
     
    // Note 2 
     rs->PutRefActiveConnection( cn ); 
     rs->Open("authors", vtMissing, adOpenStatic, adLockReadOnly, 
     adCmdTable); 
     printf("Original pagesize = %d, new pagesize = %d\n", oldPgSz, 
     rs->GetPageSize()); 
     rs->Close(); 
     cn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = %s\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
    ```

## <a name="using-getitemx-and-itemx"></a>Utilizando GetItem e Item\[x\]

Esse exemplo do Visual Basic demonstra a sintaxe padrão e alternativa para **Item**().

```vb 
 
Public Sub GetItemItem 
Dim rs As New ADODB.Recordset 
Dim name as String 
rs = rs.Open "authors", "DSN=pubs;", adOpenDynamic, _ 
 adLockBatchOptimistic, adTable 
name = rs(0) 
' -or- 
name = rs.Fields.Item(0) 
rs(0) = "Test" 
rs.UpdateBatch 
' Restore name 
rs(0) = name 
rs.UpdateBatch 
rs.Close 
End Sub 
```

Esse exemplo do Visual C++ demonstra **Item**.


> [!NOTE]
> <P>[!OBSERVAçãO] A seguinte nota corresponde às seções comentadas no exemplo de código.</P>



1.  Quando a coleção é acessada com **Item**, o índice **2** deve ser orientado para **long** para que um construtor apropriado seja chamado.
    
    ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try { 
     _RecordsetPtr rs("ADODB.Recordset"); 
     _variant_t vtFirstName; 
     
     rs->Open("authors", 
     "Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     adOpenStatic, adLockOptimistic, adCmdTable); 
     rs->MoveFirst(); 
     
    // Note 1. Get a field. 
     vtFirstName = rs->Fields->GetItem((long)2)->GetValue(); 
     // -or- 
     vtFirstName = rs->Fields->Item[(long)2]->Value; 
     
     printf( "First name = '%s'\n", (char*) ((_bstr_t) vtFirstName)); 
     
     rs->Fields->GetItem((long)2)->Value = L"TEST"; 
     rs->Update(vtMissing, vtMissing); 
     
     // Restore name 
     rs->Fields->GetItem((long)2)->PutValue(vtFirstName); 
     // -or- 
     rs->Fields->GetItem((long)2)->Value = vtFirstName; 
     rs->Update(vtMissing, vtMissing); 
     rs->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
     ::CoUninitialize(); 
    } 
    ```

## <a name="casting-ado-object-pointers-with-idispatch-"></a>Orientando ponteiros de objeto do ADO com (IDispatch \*)

O seguinte exemplo do Visual C++ demonstra o uso de (IDispatch \*) para orientar ponteiros de objetos do ADO.


> [!NOTE]
> <P>[!OBSERVAçãO] As seguintes notas correspondem às seções comentadas no exemplo de código.</P>



1.  Especifique um objeto **Connection** de abertura em uma **Variant** explicitamente codificada. Convertê-lo com (IDispatch \*) para o construtor correto seja chamado. Além disso, definir explicitamente a segunda ** \_variant\_t** parâmetro para o valor padrão **true**, portanto a contagem de referência do objeto será correta quando a operação de **Recordset** for encerrada.

2.  A expressão, (\_bstr\_t), não é uma projeção, mas um ** \_variant\_t** operador que extrai um ** \_bstr\_t** cadeia de caracteres de **Variant** retornado por **valor**. A expressão, (char\*), não é uma projeção, mas um ** \_bstr\_t** operador que extrai um ponteiro para a cadeia de caracteres encapsulado em um ** \_bstr\_t** objeto. Esta seção do código demonstra algumas dos comportamentos útil da ** \_variant\_t** e ** \_bstr\_t** operadores.
    
    ```cpp 
     
    #import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
     
    #include <stdio.h> 
     
    void main(void) 
    { 
     CoInitialize(NULL); 
     try 
     { 
     _ConnectionPtr pConn("ADODB.Connection"); 
     _RecordsetPtr pRst("ADODB.Recordset"); 
     
     pConn->Open("Provider=sqloledb;Data Source=MyServer;" 
     "Initial Catalog=pubs;Integrated Security=SSPI;", 
     "", "", adConnectUnspecified); 
    // Note 1. 
     pRst->Open( 
     "authors", 
     _variant_t((IDispatch *) pConn, true), 
     adOpenStatic, 
     adLockReadOnly, 
     adCmdTable); 
     pRst->MoveLast(); 
    // Note 2. 
     printf("Last name is '%s %s'\n", 
     (char*) ((_bstr_t) pRst->GetFields()->GetItem("au_fname")->GetValue()), 
     (char*) ((_bstr_t) pRst->Fields->Item["au_lname"]->Value)); 
     
     pRst->Close(); 
     pConn->Close(); 
     } 
     catch (_com_error &e) 
     { 
     printf("Description = '%s'\n", (char*) e.Description()); 
     } 
    ::CoUninitialize(); 
    } 
    ```

