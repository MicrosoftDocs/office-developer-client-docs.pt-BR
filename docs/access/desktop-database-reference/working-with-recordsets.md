---
title: Trabalhando com Recordsets
TOCTitle: Working with Recordsets
ms:assetid: 9cd52866-2738-8150-381c-eee0b8a6cd36
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249711(v=office.15)
ms:contentKeyID: 48546608
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0d4b877b680c80a10067e19065facd4ce9e4819d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705180"
---
# <a name="working-with-recordsets"></a>Trabalhando com Recordsets

**Aplica-se a**: Access 2013, o Office 2013 

O objeto **Recordset** tem recursos internos que tornam possível reorganizar a ordem dos dados no conjunto de resultados, para procurar um registro específico com base nos critérios fornecidos e mesmo otimizar essas operações de pesquisa usando índices. Esses recursos estão disponíveis ou não para uso dependendo do provedor e, em alguns casos,  como o da propriedade [Index](index-property-ado.md)  a estrutura da fonte de dados em si.

## <a name="arranging-data"></a>Organizando os dados

Geralmente, a maneira mais eficiente de classificar os dados em seu **Recordset** é especificando uma cláusula ORDER BY no comando SQL usado para retornar os resultados a ele. Contudo, você deve precisar alterar a ordem dos dados em um **Recordset** que já foi criado. Você pode usar a propriedade **Sort** para estabelecer a ordem na qual as linhas de um **Recordset** são percorridas. Além do mais, a propriedade **Filter** determina quais linhas podem ser acessadas ao percorrer as linhas.

A propriedade **Sort** define ou retorna um valor **String** que indica os nomes dos campos no **Recordset** que devem ser classificados. Cada nome é separado por uma vírgula e é seguido, opcionalmente, por um espaço e palavra-chave **ASC** (que classifica o campo na ordem crescente) ou **DESC** (que classifica o campo na ordem decrescente). Por padrão, se nenhuma palavra-chave for especificada, o campo será classificado na ordem crescente.

A operação sort é eficiente uma vez que os dados não são reorganizados fisicamente, mas são acessados simplesmente na ordem especificada por um índice.

A propriedade **Sort** exige que a propriedade [CursorLocation](cursorlocation-property-ado.md) seja definida como **adUseClient**. Um índice temporário será criado para cada campo especificado na propriedade **Sort** se um índice ainda não existir.

A definição da propriedade **Sort** como uma sequência vazia redefinirá as linhas para sua ordem original e excluirá os índices temporários. Os índices existentes não serão excluídos.

Suponha que um **Recordset** contém três campos chamado *"MiddleInitial"*, *firstName*e *lastName*. Definir a propriedade **Sort** com a cadeia de caracteres "", que irá ordem o **conjunto de registros** por sobrenome em ordem decrescente e depois por nome em ordem crescente. A inicial do nome do meio é ignorada.

Nenhum campo mencionado em um critério de classificação poderá ser nomeado como "ASC" ou "DESC" porque esses nomes entram em conflito com as palavras-chave **ASC** e **DESC**. Atribua um nome conflitante a um campo como um alias usando a palavra-chave **AS** na consulta que retorna o **Recordset**.

Para obter mais detalhes sobre a filtragem do **Recordset**, consulte Filtrando os resultados posteriormente neste tópico.

## <a name="finding-a-specific-record"></a>Localizando um registro específico

O ADO fornece os métodos [Find](find-method-ado.md) e [Seek](seek-method-ado.md) para localizar um determinado registro em um **Recordset**. Uma série de provedores oferece suporte ao método **Find**, mas é limitado a um único critério de pesquisa. O método **Seek** oferece suporte à pesquisa com vários critérios, mas não é suportado por muitos provedores.

Os índices nos campos podem melhorar muito o desempenho do método **Find** do objeto **Recordset** e das propriedades **Sort** e **Filter**. Você pode criar um índice interno para um objeto **Field** definindo sua propriedade dinâmica dynamic [Optimize](optimize-property-dynamic-ado.md). Esta propriedade dinâmica é adicionada à coleção **Properties** do objeto **Field** quando você define a propriedade [CursorLocation](cursorlocation-property-ado.md) como **adUseClient**. Lembre-se de que este índice é interno ao ADO  você não pode obter acesso a ele nem usá-lo para qualquer outra finalidade. Além disso, este índice é diferente da propriedade **Index** do objeto [Recordset](index-property-ado.md).

O método **Find** localiza rapidamente um valor em uma coluna (campo) de um **Recordset**. Frequentemente, você pode aumentar a velocidade da operação do método **Find** em uma coluna usando a propriedade **Optimize** para criar um índice dele.

O método **Find** limita sua pesquisa ao conteúdo de um campo. O método **Seek** exige que você tenha um índice e tenha outras limitações também. Se você precisar pesquisar em vários campos que não sejam a base de um índice ou se seu provedor não oferecer suporte aos índices, você poderá limitar seus resultados usando a propriedade **Filter** do objeto **Recordset**.

### <a name="find"></a>Find

O método **Find** procura um **Recordset** para a linha que satisfaça um critério específico. Opcionalmente, a direção da pesquisa, linha inicial e o deslocamento da linha inicial podem ser especificados. Se os critérios forem atendidos, a posição da linha atual é definida no registro encontrado; caso contrário, a posição é definida no final (ou no início) do **Recordset**, dependendo da direção da pesquisa.

Apenas um único nome de coluna pode ser especificado para o critério. Em outras palavras, este método não oferece suporte a pesquisas com várias colunas.

O operador de comparação para o critério pode ser "**\>**"(maior que),"**\<**"(menor que), "=" (igual a),"\>=" (maior que ou igual), "\<=" (menor ou igual), "\<\>" (não igual a), ou "Como" (padrão correspondente).

O valor do critério pode ser uma sequência, número do ponto flutuante ou data. Valores de cadeia de caracteres são delimitados por aspas simples ou "\#" (sinal numérico) marca (por exemplo, "estado = 'WA'" ou "estado = \#WA\#"). Valores de data são delimitados por "\#" (sinal numérico) marca (por exemplo, "Iniciar\_data \> \#22/7/97\#").

Se o operador de comparação for "like", o valor da sequência pode conter um asterisco (\*) para localizar uma ou mais ocorrências de qualquer caractere ou subsequência. Por exemplo, "state like 'M\*'" corresponde a Maine e Massachusetts. Você também pode usar asteriscos no início ou final para localizar uma subsequência contida nesses valores. Por exemplo, "state like '\*as\*'" corresponde a Alaska, Arkansas e Massachusetts.

Os asteriscos só podem ser usados no final de uma sequência de critérios ou no início e no final de uma sequência de critérios, como pode ser visto no exemplo anterior. Você não pode usar o asterisco como um caractere curinga inicial ('\*str') ou um caractere curinga incorporado ('s\*r'). Isso causará um erro.

### <a name="seek-and-index"></a>Seek e Index

Use o método **Seek** junto com a propriedade **Index** se o provedor subjacente oferecer suporte aos índices no objeto **Recordset**. Use o método [Supports](supports-method-ado.md)**(adSeek)** para determinar se o provedor subjacente oferece suporte ao método **Seek** e o método **Supports(adIndex)** para determinar se o provedor oferece suporte aos índices. (Por exemplo, o [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) oferece suporte a **Seek** e **Index**.)

Se **Seek** não localizar a linha desejada, nenhum erro ocorrerá e a linha será posicionada no final do **Recordset**. Defina a propriedade **Index** para o índice desejado antes de executar este método.

Este método é suportado apenas com os cursores do lado do servidor. Seek não é suportado quando o valor da propriedade **CursorLocation** do objeto [Recordset](cursorlocation-property-ado.md) é **adUseClient**.

Este método pode ser usado apenas quando o objeto **Recordset** foi aberto com um valor [CommandTypeEnum](commandtypeenum.md) de **adCmdTableDirect**.

## <a name="filtering-the-results"></a>Filtrando os resultados

O método **Find** limita sua pesquisa ao conteúdo de um campo. O método **Seek** exige que você tenha um índice e tenha outras limitações também. Se você precisar pesquisar em vários campos que não sejam a base de um índice ou se seu provedor não oferecer suporte aos índices, você poderá limitar seus resultados usando a propriedade **Filter** do objeto **Recordset**.

Use a propriedade **Filter** para fazer a triagem seletiva dos registros em um objeto **Recordset**. O **Recordset** filtrado torna-se o cursor atual, o que significa que os registros que não satisfaçam os critérios de **Filter** não estarão disponíveis no **Recordset** até que **Filter** seja removido. Outras propriedades que retornam valores com base no cursor atual são afetadas, como **AbsolutePosition**, **AbsolutePage**, **RecordCount** e **PageCount**. Isso ocorre porque a definição da propriedade **Filter** para um valor específico moverá o registro atual para o primeiro registro que satisfaça o novo valor.

A propriedade **Filter** assume um argumento de variante. Este valor representa um dos três métodos para usar a propriedade **Filter**: uma sequência de critérios, uma constante **FilterGroupEnum** ou uma matriz de marcadores. Para obter mais informações, consulte Filtragem com uma sequência de critérios, Filtragem com uma constante e Filtragem com marcados posteriormente neste tópico.

> [!NOTE]
> [!OBSERVAçãO] Quando você conhece os dados que deseja selecionar, geralmente é mais eficiente abrir um **Recordset** com uma instrução SQL que filtre com eficiência o conjunto de resultados, em vez de confiar na propriedade **Filter**.

Para remover um filtro de um **Recordset**, use a constante **adFilterNone**. A definição da propriedade **Filter** como uma sequência com tamanho igual a zero ("") tem o mesmo efeito que usar a constante **adFilterNone**.

### <a name="filtering-with-a-criteria-string"></a>Filtrando com uma cadeia de caracteres de critérios

A sequência de critérios é formada por cláusulas no formato *FieldName Operator Value* (por exemplo, "LastName = 'Smith'"). Você pode criar cláusulas compostas concatenando cláusulas individuais com AND (por exemplo, "LastName = 'Smith' e FirstName = 'John'") e OR (por exemplo,). Você pode criar cláusulas compostas concatenando cláusulas individuais com AND (por exemplo, "LastName = 'Smith' e FirstName = 'John'") e ou (por exemplo, "LastName = 'Smith' ou LastName = 'Jones'"). Use as seguintes diretrizes para as sequências de critérios:

- *FieldName* deve ser um nome de campo válido do **Recordset**. Se o nome do campo contiver espaços, você deverá colocar o nome entre colchetes.

- *Operator* deve ser um dos seguintes: \<, \>, \<=, \>=, \< \>, = ou LIKE.

- *É o valor com o qual você irá comparar os valores de campo* (por exemplo, 'Smith', \#8/24/95\#, 12.345 ou US $50,00). Usar aspas simples (') com cadeias de caracteres e sinais numéricos (\#) com datas. Para os números, você pode usar casas decimais, sinais de dólar e notação científica. Se o *operador* é como o *valor* pode usar caracteres curinga. Somente o asterisco (\*) e o sinal de porcentagem (%) são permitidos caracteres curinga, e devem ser o último caractere na cadeia de caracteres. *Valor* não pode ser nulo.
    
  > [!NOTE]
  > Para incluir aspas simples (') no filtro de *valor*, use aspas simples para representar um. Por exemplo, para filtrar *o ' Malley*, a sequência de critérios deve ser "col1 = ' O ' Malley'". 
  > 
  > Para incluir as marcas de aspas simples no início e no final do valor do filtro, coloque a sequência entre sinais de número (#). Por exemplo, para filtrar *'1'*, a sequência de critérios deve ser "col1 = #' 1' #".

Não há precedência entre AND e OR. As cláusulas podem ser agrupadas entre parênteses. Contudo, você não pode agrupar as cláusulas unidas por um operador OR e, em seguida, unir o grupo a outra cláusula com um operador AND, como:

```vb 
 
(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John' 
```

Ao contrário, você deveria construir esse filtro como:

```vb 
 
(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John') 
```

Em uma cláusula LIKE, você pode usar um curinga no início e no final do padrão (por exemplo, LastName Like '\*mit\*') ou apenas no final do padrão (por exemplo) ou apenas no final do padrão (por exemplo, LastName Like ' Smit\*').

### <a name="filtering-with-a-constant"></a>Filtrando com uma constante

As seguintes constantes estão disponíveis para filtrar **Recordsets**.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFilterAffectedRecords</strong></p></td>
<td><p>Filtros para visualizar apenas os registros afetados pela última chamada <strong>Delete</strong>, <strong>Resync</strong>, <strong>UpdateBatch</strong> ou <strong>CancelBatch</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFilterConflictingRecords</strong></p></td>
<td><p>Filtra para visualizar os registros que falharam na última atualização em lote.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFilterFetchedRecords</strong></p></td>
<td><p>Filtra para visualizar os registros na memória cache atual — ou seja, os resultados da última chamada para recuperar os registros do banco de dados.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFilterNone</strong></p></td>
<td><p>Remove o filtro atual e restaura todos os registros para visualização.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFilterPendingRecords</strong></p></td>
<td><p>Filtra para visualizar apenas os registros que foram alterados, mas que ainda não foram enviados ao servidor. Aplicável apenas para o modo de atualização em lote.</p></td>
</tr>
</tbody>
</table>

<br/>

As constantes do filtro se tornam mais fáceis para resolver conflitos do registro individual durante o modo de atualização de lote, permitindo que você visualize, por exemplo, apenas aqueles registros que foram afetados durante a última chamada do método **UpdateBatch**, como pode ser visto no exemplo a seguir:

```vb 
 
'BeginDeleteGroup 
    'add some bogus records 
    With objRs1 
        For i = 0 To 8 
            .AddNew 
            .Fields("CompanyName") = "Shipper Number " & i + 1 
            .Fields("Phone") = "(425) 555-000" & (i + 1) 
            .Update 
        Next i 
         
    're-connect & update 
        .ActiveConnection = GetNewConnection 
        .UpdateBatch 
         
    'filter on newly added records 
        .Filter = adFilterAffectedRecords 
        Debug.Print "Deleting the " & .RecordCount & _ 
                    " records you just added." 
         
    'delete the newly added bogus records 
        .Delete adAffectGroup 
        .Filter = adFilterNone 
        Debug.Print .RecordCount & " records remain." 
         
        .Close 
    End With 
'EndDeleteGroup 
```

### <a name="filtering-with-bookmarks"></a>Filtrando com marcadores

Finalmente, você pode passar uma matriz de variante de marcadores para a propriedade **Filter**. O cursor resultante conterá apenas aqueles registros cujo marcador foi transmitido à propriedade. O exemplo de código a seguir cria uma matriz de indicadores de registros de um **conjunto de registros** que tenham um "B" no campo *ProductName* . Em seguida, transmite a matriz para a propriedade **Filter** e exibe as informações sobre o **Recordset** filtrado resultante.

```vb 
 
'BeginFilterBkmk 
    Dim vBkmkArray() As Variant 
    Dim i As Integer 
 
    'Recordset created using "SELECT * FROM Products" as command. 
    'So, we will check to see if ProductName has a capital B, and 
    'if so, add to the array. 
    i = 0 
    Do While Not objRs.EOF 
        If InStr(1, objRs("ProductName"), "B") Then 
            ReDim Preserve vBkmkArray(i) 
            vBkmkArray(i) = objRs.Bookmark 
            i = i + 1 
            Debug.Print objRs("ProductName") 
        End If 
        objRs.MoveNext 
    Loop 
     
    'Filter using the array of bookmarks. 
    objRs.Filter = vBkmkArray 
     
    objRs.MoveFirst 
    Do While Not objRs.EOF 
        Debug.Print objRs("ProductName") 
        objRs.MoveNext 
    Loop 
    'EndFilterBkmk 
```

## <a name="creating-a-clone-of-a-recordset"></a>Criando um clone de um conjunto de registros

Use o método **Clone** para criar vários objetos **Recordset** duplicados, especialmente se você quiser mais de um registro atual em um determinado conjunto de registros. Usar o método **Clone** é mais eficiente do que criar e abrir um novo objeto **Recordset** com a mesma definição que a original.

O registro atual de um clone criado recentemente é definido originalmente para o primeiro registro. O ponteiro do registro atual em um **Recordset** clonado não é sincronizado com o original ou vice-versa. Você pode navegar independentemente em cada **Recordset**.

As alterações efetuadas em um objeto **Recordset** são visíveis em todos os seus clones, independentemente do tipo do cursor. No entanto, depois de executar [Requery](requery-method-ado.md) no **Recordset** original, os clones não mais estarão sincronizados com o original.

Fechar o **Recordset** original não faz com que suas cópias sejam fechadas nem fechar uma cópia faz com que o original seja fechado nem qualquer uma das outras cópias.

Você pode clonar um objeto **Recordset** apenas se ele oferecer suporte aos marcadores. Os valores dos marcadores podem ser intercambiados; ou seja, uma referência de marcador de um objeto **Recordset** se refere ao mesmo registro em qualquer um dos seus clones.

