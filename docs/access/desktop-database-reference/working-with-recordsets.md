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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305968"
---
# <a name="working-with-recordsets"></a><span data-ttu-id="9aad7-102">Como trabalhar com conjuntos de registros</span><span class="sxs-lookup"><span data-stu-id="9aad7-102">Working with Recordsets</span></span>

<span data-ttu-id="9aad7-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9aad7-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="9aad7-p101">O objeto **Recordset** tem recursos internos que tornam possível reorganizar a ordem dos dados no conjunto de resultados, para procurar um registro específico com base nos critérios fornecidos e mesmo otimizar essas operações de pesquisa usando índices. Esses recursos estão disponíveis ou não para uso dependendo do provedor e, em alguns casos,  como o da propriedade [Index](index-property-ado.md)  a estrutura da fonte de dados em si.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p101">The **Recordset** object has built-in features that make it possible for you to rearrange the order of the data in the result set, to search for a specific record based on criteria that you supply, and even to optimize those search operations using indexes. Whether these features are available for use depends on the provider and in some cases — such as that of the [Index](index-property-ado.md) property — the structure of the data source itself.</span></span>

## <a name="arranging-data"></a><span data-ttu-id="9aad7-106">Organizando dados</span><span class="sxs-lookup"><span data-stu-id="9aad7-106">Arranging data</span></span>

<span data-ttu-id="9aad7-p102">Geralmente, a maneira mais eficiente de classificar os dados em seu **Recordset** é especificando uma cláusula ORDER BY no comando SQL usado para retornar os resultados a ele. Contudo, você deve precisar alterar a ordem dos dados em um **Recordset** que já foi criado. Você pode usar a propriedade **Sort** para estabelecer a ordem na qual as linhas de um **Recordset** são percorridas. Além do mais, a propriedade **Filter** determina quais linhas podem ser acessadas ao percorrer as linhas.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p102">Often, the most efficient way to order the data in your **Recordset** is by specifying an ORDER BY clause in the SQL command used to return results to it. However, you might need to change the order of the data in a **Recordset** that has already been created. You can use the **Sort** property to establish the order in which rows of a **Recordset** are traversed. Furthermore, the **Filter** property determines which rows are accessible when traversing rows.</span></span>

<span data-ttu-id="9aad7-p103">A propriedade **Sort** define ou retorna um valor **String** que indica os nomes dos campos no **Recordset** que devem ser classificados. Cada nome é separado por uma vírgula e é seguido, opcionalmente, por um espaço e palavra-chave **ASC** (que classifica o campo na ordem crescente) ou **DESC** (que classifica o campo na ordem decrescente). Por padrão, se nenhuma palavra-chave for especificada, o campo será classificado na ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p103">The **Sort** property sets or returns a **String** value that indicates the field names in the **Recordset** on which to sort. Each name is separated by a comma and is optionally followed by a space and the keyword **ASC** (which sorts the field in ascending order) or **DESC** (which sorts the field in descending order). By default, if no keyword is specified, the field is sorted in ascending order.</span></span>

<span data-ttu-id="9aad7-114">A operação sort é eficiente uma vez que os dados não são reorganizados fisicamente, mas são acessados simplesmente na ordem especificada por um índice.</span><span class="sxs-lookup"><span data-stu-id="9aad7-114">The sort operation is efficient because data is not physically rearranged but is simply accessed in the order specified by an index.</span></span>

<span data-ttu-id="9aad7-p104">A propriedade **Sort** exige que a propriedade [CursorLocation](cursorlocation-property-ado.md) seja definida como **adUseClient**. Um índice temporário será criado para cada campo especificado na propriedade **Sort** se um índice ainda não existir.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p104">The **Sort** property requires the [CursorLocation](cursorlocation-property-ado.md) property to be set to **adUseClient**. A temporary index will be created for each field specified in the **Sort** property if an index does not already exist.</span></span>

<span data-ttu-id="9aad7-p105">A definição da propriedade **Sort** como uma sequência vazia redefinirá as linhas para sua ordem original e excluirá os índices temporários. Os índices existentes não serão excluídos.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p105">Setting the **Sort** property to an empty string will reset the rows to their original order and delete temporary indexes. Existing indexes will not be deleted.</span></span>

<span data-ttu-id="9aad7-119">Suponha que um **Recordset** contenha três campos denominados *firstName*, *middleInitial* e *lastName*.</span><span class="sxs-lookup"><span data-stu-id="9aad7-119">Suppose a **Recordset** contains three fields named *firstName*, *middleInitial*, and *lastName*.</span></span> <span data-ttu-id="9aad7-120">Defina a propriedade **Sort** como a cadeia de caracteres "", que ordenará o **Recordset** pelo sobrenome em ordem decrescente e, em seguida, pelo primeiro nome em ordem crescente.</span><span class="sxs-lookup"><span data-stu-id="9aad7-120">Set the **Sort** property to the string "", which will order the **Recordset** by last name in descending order and then by first name in ascending order.</span></span> <span data-ttu-id="9aad7-121">A inicial do nome do meio é ignorada.</span><span class="sxs-lookup"><span data-stu-id="9aad7-121">The middle initial is ignored.</span></span>

<span data-ttu-id="9aad7-p107">Nenhum campo mencionado em um critério de classificação poderá ser nomeado como "ASC" ou "DESC" porque esses nomes entram em conflito com as palavras-chave **ASC** e **DESC**. Atribua um nome conflitante a um campo como um alias usando a palavra-chave **AS** na consulta que retorna o **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p107">No field referenced in a sort criteria string can be named "ASC" or "DESC" because those names conflict with the keywords **ASC** and **DESC**. Give a field with a conflicting name an alias by using the **AS** keyword in the query that returns the **Recordset**.</span></span>

<span data-ttu-id="9aad7-124">Para obter mais detalhes sobre a filtragem do **Recordset**, consulte Filtrando os resultados posteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="9aad7-124">For more details about **Recordset** filtering, see Filtering the Results later in this topic.</span></span>

## <a name="finding-a-specific-record"></a><span data-ttu-id="9aad7-125">Localizar um registro específico</span><span class="sxs-lookup"><span data-stu-id="9aad7-125">Finding a specific record</span></span>

<span data-ttu-id="9aad7-p108">O ADO fornece os métodos [Find](find-method-ado.md) e [Seek](seek-method-ado.md) para localizar um determinado registro em um **Recordset**. Uma série de provedores oferece suporte ao método **Find**, mas é limitado a um único critério de pesquisa. O método **Seek** oferece suporte à pesquisa com vários critérios, mas não é suportado por muitos provedores.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p108">ADO provides the [Find](find-method-ado.md) and [Seek](seek-method-ado.md) methods for locating a particular record in a **Recordset**. The **Find** method is supported by a variety of providers but is limited to a single search criterion. The **Seek** method supports searching on multiple criteria, but is not supported by many providers.</span></span>

<span data-ttu-id="9aad7-p109">Os índices nos campos podem melhorar muito o desempenho do método **Find** do objeto **Recordset** e das propriedades **Sort** e **Filter**. Você pode criar um índice interno para um objeto **Field** definindo sua propriedade dinâmica dynamic [Optimize](optimize-property-dynamic-ado.md). Esta propriedade dinâmica é adicionada à coleção **Properties** do objeto **Field** quando você define a propriedade [CursorLocation](cursorlocation-property-ado.md) como **adUseClient**. Lembre-se de que este índice é interno ao ADO  você não pode obter acesso a ele nem usá-lo para qualquer outra finalidade. Além disso, este índice é diferente da propriedade **Index** do objeto [Recordset](index-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="9aad7-p109">Indexes on fields can greatly enhance the performance of the **Recordset** object's **Find** method and **Sort** and **Filter** properties. You can create an internal index for a **Field** object by setting its dynamic [Optimize](optimize-property-dynamic-ado.md) property. This dynamic property is added to the **Field** object's **Properties** collection when you set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**. Remember that this index is internal to ADO — you cannot gain access to it or use it for any other purpose. Also, this index is distinct from the **Recordset** object's [Index](index-property-ado.md) property.</span></span>

<span data-ttu-id="9aad7-p110">O método **Find** localiza rapidamente um valor em uma coluna (campo) de um **Recordset**. Frequentemente, você pode aumentar a velocidade da operação do método **Find** em uma coluna usando a propriedade **Optimize** para criar um índice dele.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p110">The **Find** method quickly locates a value within a column (field) of a **Recordset**. You can often improve the speed of the **Find** method's operation on a column by using the **Optimize** property to create an index on it.</span></span>

<span data-ttu-id="9aad7-p111">O método **Find** limita sua pesquisa ao conteúdo de um campo. O método **Seek** exige que você tenha um índice e tenha outras limitações também. Se você precisar pesquisar em vários campos que não sejam a base de um índice ou se seu provedor não oferecer suporte aos índices, você poderá limitar seus resultados usando a propriedade **Filter** do objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p111">The **Find** method limits your search to the contents of one field. The **Seek** method requires that you have an index and has other limitations as well. If you need to search on multiple fields that aren't the basis of an index, or if your provider does not support indexes, you can limit your results using the **Filter** property of the **Recordset** object.</span></span>

### <a name="find"></a><span data-ttu-id="9aad7-139">Localizar</span><span class="sxs-lookup"><span data-stu-id="9aad7-139">Find</span></span>

<span data-ttu-id="9aad7-p112">O método **Find** procura um **Recordset** para a linha que satisfaça um critério específico. Opcionalmente, a direção da pesquisa, linha inicial e o deslocamento da linha inicial podem ser especificados. Se os critérios forem atendidos, a posição da linha atual é definida no registro encontrado; caso contrário, a posição é definida no final (ou no início) do **Recordset**, dependendo da direção da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p112">The **Find** method searches a **Recordset** for the row that satisfies a specified criterion. Optionally, the direction of the search, starting row, and offset from the starting row may be specified. If the criterion is met, the current row position is set on the found record; otherwise, the position is set to the end (or start) of the **Recordset**, depending on search direction.</span></span>

<span data-ttu-id="9aad7-p113">Apenas um único nome de coluna pode ser especificado para o critério. Em outras palavras, este método não oferece suporte a pesquisas com várias colunas.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p113">Only a single-column name may be specified for the criterion. In other words, this method does not support multi-column searches.</span></span>

<span data-ttu-id="9aad7-145">O operador de comparação para o critério pode ser**\>**"" (maior que),**\<**"" (menor que), "=" (igual),\>"=" (maior que ou igual a)\<, "=" (menor ou igual),\<\>"" (não igual) ou "Like" (correspondência de padrão).</span><span class="sxs-lookup"><span data-stu-id="9aad7-145">The comparison operator for the criterion may be "**\>**" (greater than), "**\<**" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "LIKE" (pattern matching).</span></span>

<span data-ttu-id="9aad7-146">O valor do critério pode ser uma sequência, número do ponto flutuante ou data.</span><span class="sxs-lookup"><span data-stu-id="9aad7-146">The criterion value may be a string, floating-point number, or date.</span></span> <span data-ttu-id="9aad7-147">Valores de cadeia de caracteres são delimitados por\#aspas simples ou marcas "" (sinal de número) (por exemplo, "State = ' wa ' \#"\#ou "state = WA").</span><span class="sxs-lookup"><span data-stu-id="9aad7-147">String values are delimited with single quotes or "\#" (number sign) marks (for example, "state = 'WA'" or "state = \#WA\#").</span></span> <span data-ttu-id="9aad7-148">os valores de data são\#delimitados com marcas "" (sinal de número) (por\_exemplo \> \#,\#"data de início 7/22/97").</span><span class="sxs-lookup"><span data-stu-id="9aad7-148">Date values are delimited with "\#" (number sign) marks (for example, "start\_date \> \#7/22/97\#").</span></span>

<span data-ttu-id="9aad7-p115">Se o operador de comparação for "like", o valor da sequência pode conter um asterisco (\*) para localizar uma ou mais ocorrências de qualquer caractere ou subsequência. Por exemplo, "state like 'M\*'" corresponde a Maine e Massachusetts. Você também pode usar asteriscos no início ou final para localizar uma subsequência contida nesses valores. Por exemplo, "state like '\*as\*'" corresponde a Alaska, Arkansas e Massachusetts.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p115">If the comparison operator is "like", the string value may contain an asterisk (\*) to find one or more occurrences of any character or substring. For example, "state like 'M\*'" matches Maine and Massachusetts. You can also use leading and trailing asterisks to find a substring contained within the values. For example, "state like '\*as\*'" matches Alaska, Arkansas, and Massachusetts.</span></span>

<span data-ttu-id="9aad7-p116">Os asteriscos só podem ser usados no final de uma sequência de critérios ou no início e no final de uma sequência de critérios, como pode ser visto no exemplo anterior. Você não pode usar o asterisco como um caractere curinga inicial ('\*str') ou um caractere curinga incorporado ('s\*r'). Isso causará um erro.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p116">Asterisks can be used only at the end of a criteria string or together at both the beginning and end of a criteria string, as shown above. You cannot use the asterisk as a leading wildcard ('\*str') or embedded wildcard ('s\*r'). This will cause an error.</span></span>

### <a name="seek-and-index"></a><span data-ttu-id="9aad7-156">Seek e Index</span><span class="sxs-lookup"><span data-stu-id="9aad7-156">Seek and Index</span></span>

<span data-ttu-id="9aad7-p117">Use o método **Seek** junto com a propriedade **Index** se o provedor subjacente oferecer suporte aos índices no objeto **Recordset**. Use o método [Supports](supports-method-ado.md)**(adSeek)** para determinar se o provedor subjacente oferece suporte ao método **Seek** e o método **Supports(adIndex)** para determinar se o provedor oferece suporte aos índices. (Por exemplo, o [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) oferece suporte a **Seek** e **Index**.)</span><span class="sxs-lookup"><span data-stu-id="9aad7-p117">Use the **Seek** method in conjunction with the **Index** property if the underlying provider supports indexes on the **Recordset** object. Use the [Supports](supports-method-ado.md)**(adSeek)** method to determine whether the underlying provider supports **Seek**, and the **Supports(adIndex)** method to determine whether the provider supports indexes. (For example, the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) supports **Seek** and **Index**.)</span></span>

<span data-ttu-id="9aad7-p118">Se **Seek** não localizar a linha desejada, nenhum erro ocorrerá e a linha será posicionada no final do **Recordset**. Defina a propriedade **Index** para o índice desejado antes de executar este método.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p118">If **Seek** does not find the desired row, no error occurs, and the row is positioned at the end of the **Recordset**. Set the **Index** property to the desired index before executing this method.</span></span>

<span data-ttu-id="9aad7-p119">Este método é suportado apenas com os cursores do lado do servidor. Seek não é suportado quando o valor da propriedade **CursorLocation** do objeto [Recordset](cursorlocation-property-ado.md) é **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p119">This method is supported only with server-side cursors. Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.</span></span>

<span data-ttu-id="9aad7-164">Este método pode ser usado apenas quando o objeto **Recordset** foi aberto com um valor [CommandTypeEnum](commandtypeenum.md) de **adCmdTableDirect**.</span><span class="sxs-lookup"><span data-stu-id="9aad7-164">This method can be used only when the **Recordset** object has been opened with a [CommandTypeEnum](commandtypeenum.md) value of **adCmdTableDirect**.</span></span>

## <a name="filtering-the-results"></a><span data-ttu-id="9aad7-165">Filtrando os resultados</span><span class="sxs-lookup"><span data-stu-id="9aad7-165">Filtering the results</span></span>

<span data-ttu-id="9aad7-p120">O método **Find** limita sua pesquisa ao conteúdo de um campo. O método **Seek** exige que você tenha um índice e tenha outras limitações também. Se você precisar pesquisar em vários campos que não sejam a base de um índice ou se seu provedor não oferecer suporte aos índices, você poderá limitar seus resultados usando a propriedade **Filter** do objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p120">The **Find** method limits your search to the contents of one field. The **Seek** method requires that you have an index and has other limitations as well. If you need to search on multiple fields that are not the basis of an index or if your provider does not support indexes, you can limit your results using the **Filter** property of the **Recordset** object.</span></span>

<span data-ttu-id="9aad7-p121">Use a propriedade **Filter** para fazer a triagem seletiva dos registros em um objeto **Recordset**. O **Recordset** filtrado torna-se o cursor atual, o que significa que os registros que não satisfaçam os critérios de **Filter** não estarão disponíveis no **Recordset** até que **Filter** seja removido. Outras propriedades que retornam valores com base no cursor atual são afetadas, como **AbsolutePosition**, **AbsolutePage**, **RecordCount** e **PageCount**. Isso ocorre porque a definição da propriedade **Filter** para um valor específico moverá o registro atual para o primeiro registro que satisfaça o novo valor.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p121">Use the **Filter** property to selectively screen out records in a **Recordset** object. The filtered **Recordset** becomes the current cursor, which means that records that do not satisfy the **Filter** criteria are not available in the **Recordset** until the **Filter** is removed. Other properties that return values based on the current cursor are affected, such as **AbsolutePosition**, **AbsolutePage**, **RecordCount**, and **PageCount**. This is because setting the **Filter** property to a specific value will move the current record to the first record that satisfies the new value.</span></span>

<span data-ttu-id="9aad7-p122">A propriedade **Filter** assume um argumento de variante. Este valor representa um dos três métodos para usar a propriedade **Filter**: uma sequência de critérios, uma constante **FilterGroupEnum** ou uma matriz de marcadores. Para obter mais informações, consulte Filtragem com uma sequência de critérios, Filtragem com uma constante e Filtragem com marcados posteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p122">The **Filter** property takes a variant argument. This value represents one of three methods for using the **Filter** property: a criteria string, a **FilterGroupEnum** constant, or an array of bookmarks. For more information, see Filtering with a Criteria String, Filtering with a Constant, and Filtering with Bookmarks later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="9aad7-176">[!OBSERVAçãO] Quando você conhece os dados que deseja selecionar, geralmente é mais eficiente abrir um **Recordset** com uma instrução SQL que filtre com eficiência o conjunto de resultados, em vez de confiar na propriedade **Filter**.</span><span class="sxs-lookup"><span data-stu-id="9aad7-176">When you know the data you want to select, it is usually more efficient to open a **Recordset** with a SQL statement that effectively filters the result set, rather than relying on the **Filter** property.</span></span>

<span data-ttu-id="9aad7-p123">Para remover um filtro de um **Recordset**, use a constante **adFilterNone**. A definição da propriedade **Filter** como uma sequência com tamanho igual a zero ("") tem o mesmo efeito que usar a constante **adFilterNone**.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p123">To remove a filter from a **Recordset**, use the **adFilterNone** constant. Setting the **Filter** property to a zero-length string ("") has the same effect as using the **adFilterNone** constant.</span></span>

### <a name="filtering-with-a-criteria-string"></a><span data-ttu-id="9aad7-179">Filtragem com uma cadeia de caracteres de critérios</span><span class="sxs-lookup"><span data-stu-id="9aad7-179">Filtering with a criteria string</span></span>

<span data-ttu-id="9aad7-180">A cadeia de caracteres de critérios é composta por cláusulas no *valor do operador FieldName* do formulário (por exemplo, "LastName = ' Smith '").</span><span class="sxs-lookup"><span data-stu-id="9aad7-180">The criteria string is made up of clauses in the form *FieldName Operator Value* (for example, "LastName = 'Smith'").</span></span> <span data-ttu-id="9aad7-181">Você pode criar cláusulas compostas concatenando cláusulas individuais com AND (por exemplo, "LastName = ' Smith ' e FirstName = ' John '") e OR (por exemplo,).</span><span class="sxs-lookup"><span data-stu-id="9aad7-181">You can create compound clauses by concatenating individual clauses with AND (for example, "LastName = 'Smith' AND FirstName = 'John'") and OR (for example, ).</span></span> <span data-ttu-id="9aad7-182">Você pode criar cláusulas compostas concatenando cláusulas individuais com AND (por exemplo, "LastName = ' Smith ' e FirstName = ' John '") e ou (por exemplo, "LastName = ' Smith ' ou LastName = ' Jones '").</span><span class="sxs-lookup"><span data-stu-id="9aad7-182">You can create compound clauses by concatenating individual clauses with AND (for example, "LastName = 'Smith' AND FirstName = 'John'") and OR (for example, "LastName = 'Smith' OR LastName = 'Jones'").</span></span> <span data-ttu-id="9aad7-183">Use as seguintes diretrizes para as sequências de critérios:</span><span class="sxs-lookup"><span data-stu-id="9aad7-183">Use the following guidelines for criteria strings:</span></span>

- <span data-ttu-id="9aad7-p125">*FieldName* deve ser um nome de campo válido do **Recordset**. Se o nome de campo contiver espaços, coloque o nome entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p125">*FieldName* must be a valid field name from the **Recordset**. If the field name contains spaces, you must enclose the name in square brackets.</span></span>

- <span data-ttu-id="9aad7-186">*Operator* deve ser uma das seguintes opções: \<, \>, \<=, \>=, \< \>, = ou like.</span><span class="sxs-lookup"><span data-stu-id="9aad7-186">*Operator* must be one of the following: \<, \>, \<=, \>=, \<\>, =, or LIKE.</span></span>

- <span data-ttu-id="9aad7-187">*Value* é o valor com o qual você irá comparar os valores de campo (por exemplo, ' Smith \#'\#, 8/24/95, 12,345 ou $50).</span><span class="sxs-lookup"><span data-stu-id="9aad7-187">*Value* is the value with which you will compare the field values (for example, 'Smith', \#8/24/95\#, 12.345, or $50.00).</span></span> <span data-ttu-id="9aad7-188">Use aspas simples (') com cadeias de caracteres e sinais\#de sustenido () com datas.</span><span class="sxs-lookup"><span data-stu-id="9aad7-188">Use single quotation marks (') with strings and pound signs (\#) with dates.</span></span> <span data-ttu-id="9aad7-189">Para os números, você pode usar casas decimais, sinais de dólar e notação científica.</span><span class="sxs-lookup"><span data-stu-id="9aad7-189">For numbers, you can use decimal points, dollar signs, and scientific notation.</span></span> <span data-ttu-id="9aad7-190">Se o *Operator* for LIKE, *Value* poderá usar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="9aad7-190">If *Operator* is LIKE, *Value* can use wildcards.</span></span> <span data-ttu-id="9aad7-191">Somente o asterisco (\*) e o sinal de porcentagem (%) os curingas são permitidos e devem ser o último caractere na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9aad7-191">Only the asterisk (\*) and percent sign (%) wildcards are allowed, and they must be the last character in the string.</span></span> <span data-ttu-id="9aad7-192">*Value* não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="9aad7-192">*Value* cannot be null.</span></span>
    
  > [!NOTE]
  > <span data-ttu-id="9aad7-193">Para incluir aspas simples (') no filtro *Value*, use duas aspas simples para representar uma.</span><span class="sxs-lookup"><span data-stu-id="9aad7-193">To include single quotation marks (') in the filter *Value*, use two single quotation marks to represent one.</span></span> <span data-ttu-id="9aad7-194">Por exemplo, para filtrar no *' Malley*, a cadeia de caracteres de critérios deve ser "Col1 = ' O ' ' Malley '".</span><span class="sxs-lookup"><span data-stu-id="9aad7-194">For example, to filter on *O'Malley*, the criteria string should be "col1 = 'O''Malley'".</span></span> 
  > 
  > <span data-ttu-id="9aad7-195">Para incluir as marcas de aspas simples no início e no final do valor do filtro, coloque a sequência entre sinais de número (#).</span><span class="sxs-lookup"><span data-stu-id="9aad7-195">To include single quotation marks at both the beginning and the end of the filter value, enclose the string in pound signs (#).</span></span> <span data-ttu-id="9aad7-196">Por exemplo, para filtrar em *' 1 '*, a sequência de critérios deve ser "Col1 = # ' 1 ' #".</span><span class="sxs-lookup"><span data-stu-id="9aad7-196">For example, to filter on *'1'*, the criteria string should be "col1 = #'1'#".</span></span>

<span data-ttu-id="9aad7-p129">Não há precedência entre AND e OR. As cláusulas podem ser agrupadas entre parênteses. Contudo, você não pode agrupar as cláusulas unidas por um operador OR e, em seguida, unir o grupo a outra cláusula com um operador AND, como:</span><span class="sxs-lookup"><span data-stu-id="9aad7-p129">There is no precedence between AND and OR. Clauses can be grouped within parentheses. However, you cannot group clauses joined by an OR and then join the group to another clause with an AND, like this:</span></span>

```vb 
 
(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John' 
```

<span data-ttu-id="9aad7-200">Ao contrário, você deveria construir esse filtro como:</span><span class="sxs-lookup"><span data-stu-id="9aad7-200">Instead, you would construct this filter as:</span></span>

```vb 
 
(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John') 
```

<span data-ttu-id="9aad7-201">Em uma cláusula LIKE, você pode usar um curinga no início e no final do padrão (por exemplo, LastName como '\*MIT\*') ou apenas no final do padrão (por exemplo,) ou apenas no final do padrão (por exemplo, LastName como ' Smit\*').</span><span class="sxs-lookup"><span data-stu-id="9aad7-201">In a LIKE clause, you can use a wildcard at the beginning and end of the pattern (for example, LastName Like '\*mit\*') or only at the end of the pattern (for example, ) or only at the end of the pattern (for example, LastName Like 'Smit\*').</span></span>

### <a name="filtering-with-a-constant"></a><span data-ttu-id="9aad7-202">Filtrando com uma constante</span><span class="sxs-lookup"><span data-stu-id="9aad7-202">Filtering with a constant</span></span>

<span data-ttu-id="9aad7-203">As seguintes constantes estão disponíveis para filtrar **Recordsets**.</span><span class="sxs-lookup"><span data-stu-id="9aad7-203">The following constants are available for filtering **Recordsets**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9aad7-204">Constante</span><span class="sxs-lookup"><span data-stu-id="9aad7-204">Constant</span></span></p></th>
<th><p><span data-ttu-id="9aad7-205">Descrição</span><span class="sxs-lookup"><span data-stu-id="9aad7-205">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9aad7-206"><strong>adFilterAffectedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="9aad7-206"><strong>adFilterAffectedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="9aad7-207">Filtros para visualizar apenas os registros afetados pela última chamada <strong>Delete</strong>, <strong>Resync</strong>, <strong>UpdateBatch</strong> ou <strong>CancelBatch</strong>.</span><span class="sxs-lookup"><span data-stu-id="9aad7-207">Filters for viewing only records effected by the last <strong>Delete</strong>, <strong>Resync</strong>, <strong>UpdateBatch</strong>, or <strong>CancelBatch</strong> call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aad7-208"><strong>adFilterConflictingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="9aad7-208"><strong>adFilterConflictingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="9aad7-209">Filtra para visualizar os registros que falharam na última atualização em lote.</span><span class="sxs-lookup"><span data-stu-id="9aad7-209">Filters for viewing the records that failed the last batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aad7-210"><strong>adFilterFetchedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="9aad7-210"><strong>adFilterFetchedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="9aad7-211">Filtra para visualizar os registros na memória cache atual — ou seja, os resultados da última chamada para recuperar os registros do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="9aad7-211">Filters for viewing the records in the current cache — that is, the results of the last call to retrieve records from the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9aad7-212"><strong>adFilterNone</strong></span><span class="sxs-lookup"><span data-stu-id="9aad7-212"><strong>adFilterNone</strong></span></span></p></td>
<td><p><span data-ttu-id="9aad7-213">Remove o filtro atual e restaura todos os registros para visualização.</span><span class="sxs-lookup"><span data-stu-id="9aad7-213">Removes the current filter and restores all records for viewing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9aad7-214"><strong>adFilterPendingRecords</strong></span><span class="sxs-lookup"><span data-stu-id="9aad7-214"><strong>adFilterPendingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="9aad7-215">Filtra para visualizar apenas os registros que foram alterados, mas que ainda não foram enviados ao servidor.</span><span class="sxs-lookup"><span data-stu-id="9aad7-215">Filters for viewing only records that have changed but have not yet been sent to the server.</span></span> <span data-ttu-id="9aad7-216">Aplicável apenas para o modo de atualização em lote.</span><span class="sxs-lookup"><span data-stu-id="9aad7-216">Applicable only for batch update mode.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="9aad7-217">As constantes do filtro se tornam mais fáceis para resolver conflitos do registro individual durante o modo de atualização de lote, permitindo que você visualize, por exemplo, apenas aqueles registros que foram afetados durante a última chamada do método **UpdateBatch**, como pode ser visto no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="9aad7-217">The filter constants make it easier to resolve individual record conflicts during batch update mode by allowing you to view, for example, only those records that were effected during the last **UpdateBatch** method call, as shown in the following example:</span></span>

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

### <a name="filtering-with-bookmarks"></a><span data-ttu-id="9aad7-218">Filtrando com indicadores</span><span class="sxs-lookup"><span data-stu-id="9aad7-218">Filtering with bookmarks</span></span>

<span data-ttu-id="9aad7-p131">Finalmente, você pode passar uma matriz de variante de marcadores para a propriedade **Filter**. O cursor resultante conterá apenas aqueles registros cujo marcador foi transmitido à propriedade. O seguinte exemplo de código cria uma matriz de marcadores a partir dos registros em um **Recordset** que tenha um "B" no campo *ProductName*. Em seguida, transmite a matriz para a propriedade **Filter** e exibe as informações sobre o **Recordset** filtrado resultante.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p131">Finally, you can pass a variant array of bookmarks to the **Filter** property. The resulting cursor will contain only those records whose bookmark was passed in to the property. The following code example creates an array of bookmarks from the records in a **Recordset** which have a "B" in the *ProductName* field. It then passes the array to the **Filter** property and displays information about the resulting filtered **Recordset**.</span></span>

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

## <a name="creating-a-clone-of-a-recordset"></a><span data-ttu-id="9aad7-223">Criando um clone de um Recordset</span><span class="sxs-lookup"><span data-stu-id="9aad7-223">Creating a clone of a Recordset</span></span>

<span data-ttu-id="9aad7-p132">Use o método **Clone** para criar vários objetos **Recordset** duplicados, especialmente se você quiser mais de um registro atual em um determinado conjunto de registros. Usar o método **Clone** é mais eficiente do que criar e abrir um novo objeto **Recordset** com a mesma definição que a original.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p132">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records. Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="9aad7-p133">O registro atual de um clone criado recentemente é definido originalmente para o primeiro registro. O ponteiro do registro atual em um **Recordset** clonado não é sincronizado com o original ou vice-versa. Você pode navegar independentemente em cada **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p133">The current record of a newly created clone is originally set to the first record. The current record pointer in a cloned **Recordset** is not synchronized with the original or vice versa. You can navigate independently in each **Recordset**.</span></span>

<span data-ttu-id="9aad7-p134">As alterações efetuadas em um objeto **Recordset** são visíveis em todos os seus clones, independentemente do tipo do cursor. No entanto, depois de executar [Requery](requery-method-ado.md) no **Recordset** original, os clones não mais estarão sincronizados com o original.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p134">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type. However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="9aad7-231">Fechar o **Recordset** original não faz com que suas cópias sejam fechadas nem fechar uma cópia faz com que o original seja fechado nem qualquer uma das outras cópias.</span><span class="sxs-lookup"><span data-stu-id="9aad7-231">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="9aad7-p135">Você pode clonar um objeto **Recordset** apenas se ele oferecer suporte aos marcadores. Os valores dos marcadores podem ser intercambiados; ou seja, uma referência de marcador de um objeto **Recordset** se refere ao mesmo registro em qualquer um dos seus clones.</span><span class="sxs-lookup"><span data-stu-id="9aad7-p135">You can clone a **Recordset** object only if it supports bookmarks. Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>

