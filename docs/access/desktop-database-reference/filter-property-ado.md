---
<span data-ttu-id="fd9d9-101"><<<<<<< Título cabeça: propriedade Filter (ADO) TOCTitle: propriedade Filter (ADO) === título: propriedade Filter (ADO) TOCTitle: propriedade Filter (ADO)</span><span class="sxs-lookup"><span data-stu-id="fd9d9-101"><<<<<<< HEAD title: Filter Property (ADO) TOCTitle: Filter Property (ADO) ======= title: Filter property (ADO) TOCTitle: Filter property (ADO)</span></span>
>>>>>>> <span data-ttu-id="fd9d9-102">ms:assetid de mestre: 5abc528a-a6ee-34de-5d44-a3249194b0a0 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249314(v=office.15) ms:contentKeyID: ms.date 48545053: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="fd9d9-102">master ms:assetid: 5abc528a-a6ee-34de-5d44-a3249194b0a0 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249314(v=office.15) ms:contentKeyID: 48545053 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="fd9d9-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="fd9d9-103"><<<<<<< HEAD</span></span>
# <a name="filter-property-ado"></a><span data-ttu-id="fd9d9-104">Propriedade Filter (ADO)</span><span class="sxs-lookup"><span data-stu-id="fd9d9-104">Filter Property (ADO)</span></span>
=======
# <a name="filter-property-ado"></a><span data-ttu-id="fd9d9-105">Propriedade Filter (ADO)</span><span class="sxs-lookup"><span data-stu-id="fd9d9-105">Filter property (ADO)</span></span>
>>>>>>> <span data-ttu-id="fd9d9-106">mestre</span><span class="sxs-lookup"><span data-stu-id="fd9d9-106">master</span></span>


<span data-ttu-id="fd9d9-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fd9d9-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fd9d9-108">Indica um filtro para os dados em um [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="fd9d9-108">Indicates a filter for data in a [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="fd9d9-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="fd9d9-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="fd9d9-110">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fd9d9-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="fd9d9-111">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="fd9d9-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="fd9d9-112">mestre</span><span class="sxs-lookup"><span data-stu-id="fd9d9-112">master</span></span>

<span data-ttu-id="fd9d9-113">Define ou retorna um valor **Variant**, que pode conter:</span><span class="sxs-lookup"><span data-stu-id="fd9d9-113">Sets or returns a **Variant** value, which can contain one of the following:</span></span>

  - <span data-ttu-id="fd9d9-114">**Sequência de critérios**  uma cadeia de caracteres formada por uma ou mais cláusulas individuais concatenadas com os operadores **AND** ou **OR**.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-114">**Criteria string** — a string made up of one or more individual clauses concatenated with **AND** or **OR** operators.</span></span>

  - <span data-ttu-id="fd9d9-115">**Matriz de indicadores**  uma matriz de valores de indicadores exclusivos que apontam para registros no objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-115">**Array of bookmarks** — an array of unique bookmark values that point to records in the **Recordset** object.</span></span>

  - <span data-ttu-id="fd9d9-116">Um valor [FilterGroupEnum](filtergroupenum.md).</span><span class="sxs-lookup"><span data-stu-id="fd9d9-116">A [FilterGroupEnum](filtergroupenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd9d9-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd9d9-117">Remarks</span></span>

<span data-ttu-id="fd9d9-p101">Use a propriedade **Filter** para filtrar de maneira seletiva os registros de um objeto **Recordset**. O **Recordset** filtrado torna-se o cursor atual. Outras propriedades que retornam valores com base no cursor atual são afetadas, como [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), [RecordCount](recordcount-property-ado.md) e [PageCount](pagecount-property-ado.md). Isso ocorre porque definir a propriedade **Filter** para um valor específico moverá o registro atual para o primeiro registro que atende ao novo valor.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-p101">Use the **Filter** property to selectively screen out records in a **Recordset** object. The filtered **Recordset** becomes the current cursor. Other properties that return values based on the current cursor are affected, such as [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), [RecordCount](recordcount-property-ado.md), and [PageCount](pagecount-property-ado.md). This is because setting the **Filter** property to a specific value will move the current record to the first record that satisfies the new value.</span></span>

<span data-ttu-id="fd9d9-122">A sequência de critérios é formada por cláusulas no formulário *FieldName-Operator-Value* (por exemplo, "LastName = 'Smith'").</span><span class="sxs-lookup"><span data-stu-id="fd9d9-122">The criteria string is made up of clauses in the form *FieldName-Operator-Value* (for example, "LastName = 'Smith'").</span></span> <span data-ttu-id="fd9d9-123">Você pode criar cláusulas compostas concatenando cláusulas individuais com **AND** (por exemplo, "LastName = 'Smith' e FirstName = 'John'") ou **OR** (por exemplo, ").</span><span class="sxs-lookup"><span data-stu-id="fd9d9-123">You can create compound clauses by concatenating individual clauses with **AND** (for example, "LastName = 'Smith' AND FirstName = 'John'") or **OR** (for example, ").</span></span> <span data-ttu-id="fd9d9-124">Você pode criar cláusulas compostas concatenando cláusulas individuais com **AND** (por exemplo, "LastName = 'Smith' e FirstName = 'John'") ou **OR** (por exemplo, "LastName = 'Smith' ou LastName = 'Jones'").</span><span class="sxs-lookup"><span data-stu-id="fd9d9-124">You can create compound clauses by concatenating individual clauses with **AND** (for example, "LastName = 'Smith' AND FirstName = 'John'") or **OR** (for example, "LastName = 'Smith' OR LastName = 'Jones'").</span></span> <span data-ttu-id="fd9d9-125">Use as seguintes diretrizes para as sequências de critérios:</span><span class="sxs-lookup"><span data-stu-id="fd9d9-125">Use the following guidelines for criteria strings:</span></span>

  - <span data-ttu-id="fd9d9-126">*FieldName* deve ser um nome de campo válido do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-126">*FieldName* must be a valid field name from the **Recordset**.</span></span> <span data-ttu-id="fd9d9-127">Se o nome do campo contiver espaços, você deverá colocar o nome entre colchetes.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-127">If the field name contains spaces, you must enclose the name in square brackets.</span></span>

  - <span data-ttu-id="fd9d9-128">*Operator* deve ser um dos seguintes: \<, \>, \<=, \>=, \< \>, inglês, ou **como**.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-128">*Operator* must be one of the following: \<, \>, \<=, \>=, \<\>, =, or **LIKE**.</span></span>

  - <span data-ttu-id="fd9d9-129">*É o valor com o qual você irá comparar os valores de campo* (por exemplo, 'Smith', \#8/24/95\#, 12.345 ou US $50,00).</span><span class="sxs-lookup"><span data-stu-id="fd9d9-129">*Value* is the value with which you will compare the field values (for example, 'Smith', \#8/24/95\#, 12.345, or $50.00).</span></span> <span data-ttu-id="fd9d9-130">Usar aspas simples com cadeias de caracteres e sinais numéricos (\#) com datas.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-130">Use single quotes with strings and pound signs (\#) with dates.</span></span> <span data-ttu-id="fd9d9-131">Para os números, você pode usar casas decimais, sinais de dólar e notação científica.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-131">For numbers, you can use decimal points, dollar signs, and scientific notation.</span></span> <span data-ttu-id="fd9d9-132">Se o *operador* é **SEMELHANTE**, o *valor* pode usar caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-132">If *Operator* is **LIKE**, *Value* can use wildcards.</span></span> <span data-ttu-id="fd9d9-133">Somente o asterisco (\*) e o sinal de porcentagem (%) caracteres curinga é permitida, e eles devem ser o último caractere na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-133">Only the asterisk (\*) and percent sign (%) wild cards are allowed, and they must be the last character in the string.</span></span> <span data-ttu-id="fd9d9-134">*Valor* não pode ser nulo.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-134">*Value* cannot be null.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="fd9d9-p105">[!OBSERVAçãO] Para incluir aspas simples (') no filtro Value, use duas aspas simples para representar uma. Por exemplo, para filtrar em O'Malley, a sequência de critérios deve ser "col1 = 'O''Malley'". Para incluir aspas simples no início e no final do valor de filtragem, coloque a sequência entre símbolos de libra (#). Por exemplo, para filtrar em '1', a sequência de critérios deve ser "col1 = #'1'#".</span><span class="sxs-lookup"><span data-stu-id="fd9d9-p105">To include single quotation marks (') in the filter Value, use two single quotation marks to represent one. For example, to filter on O'Malley, the criteria string should be "col1 = 'O''Malley'". To include single quotation marks at both the beginning and the end of the filter value, enclose the string with pound signs (#). For example, to filter on '1', the criteria string should be "col1 = #'1'#".</span></span></P>



  - <span data-ttu-id="fd9d9-p106">Não há precedência entre **AND** e **OR**. As cláusulas podem ser agrupadas entre parênteses. No entanto, não é possível agrupar as cláusulas unidas por um **OR** e, em seguida, unir o grupo a outra cláusula com um **AND**, como neste exemplo:</span><span class="sxs-lookup"><span data-stu-id="fd9d9-p106">There is no precedence between **AND** and **OR**. Clauses can be grouped within parentheses. However, you cannot group clauses joined by an **OR** and then join the group to another clause with an **AND**, like this:</span></span>

  - <span data-ttu-id="fd9d9-142">Em vez disso, você deve construir esse filtro como</span><span class="sxs-lookup"><span data-stu-id="fd9d9-142">Instead, you would construct this filter as</span></span>

  - <span data-ttu-id="fd9d9-143">Em uma cláusula **LIKE** , você pode usar um curinga no início e no final do padrão (por exemplo, LastName Like '\*mit\*'), ou apenas no final do padrão (por exemplo, LastName Like ' Smit\*').</span><span class="sxs-lookup"><span data-stu-id="fd9d9-143">In a **LIKE** clause, you can use a wildcard at the beginning and end of the pattern (for example, LastName Like '\*mit\*'), or only at the end of the pattern (for example, LastName Like 'Smit\*').</span></span>

<span data-ttu-id="fd9d9-144">As constantes de filtragem tornam mais fácil resolver conflitos individuais de registro durante o modo de atualização em lote, permitindo que você exiba, por exemplo, apenas os registros que foram afetados durante a última chamada do método [UpdateBatch](updatebatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="fd9d9-144">The filter constants make it easier to resolve individual record conflicts during batch update mode by allowing you to view, for example, only those records that were affected during the last [UpdateBatch](updatebatch-method-ado.md) method call.</span></span>

<span data-ttu-id="fd9d9-p107">A definição da propriedade **Filter** pode falhar devido a um conflito com os dados de base (por exemplo, um registro já foi excluído por outro usuário). Nesse caso, o provedorretorna avisos para a coleção [Errors](errors-collection-ado.md), mas não paralisa a execução do programa. Um erro de tempo de execução ocorre apenas quando houver conflitos em todos os registros solicitados. Use a propriedade [Status](status-property-ado-recordset.md) para localizar registros com conflitos.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-p107">Setting the **Filter** property itself may fail because of a conflict with the underlying data (for example, a record has already been deleted by another user). In such a case, the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records. Use the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="fd9d9-149">Definir a propriedade **Filter** para uma sequência de comprimento zero ("") tem o mesmo efeito que usar a constante **adFilterNone**.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-149">Setting the **Filter** property to a zero-length string ("") has the same effect as using the **adFilterNone** constant.</span></span>

<span data-ttu-id="fd9d9-p108">Sempre que a propriedade **Filter** for definida, a posição atual do registro passará para o primeiro registro no subconjunto filtrado de registros no **Recordset**. Da mesma forma, quando a propriedade **Filter** estiver em branco, a posição atual do registro passará para o primeiro registro no **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-p108">Whenever the **Filter** property is set, the current record position moves to the first record in the filtered subset of records in the **Recordset**. Similarly, when the **Filter** property is cleared, the current record position moves to the first record in the **Recordset**.</span></span>

<span data-ttu-id="fd9d9-152">Consulte a propriedade [Bookmark](bookmark-property-ado.md) para obter uma explicação sobre valores de indicadores a partir dos quais é possível construir uma matriz para usar com a propriedade **Filter**.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-152">See the [Bookmark](bookmark-property-ado.md) property for an explanation of bookmark values from which you can build an array to use with the **Filter** property.</span></span>

<span data-ttu-id="fd9d9-153">Somente os **filtros** no formato de cadeias de caracteres de critérios (ex.: DataDoPedido \> ' 12/31/1999 ') afetam o conteúdo de um **Recordset**de persistido.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-153">Only **Filters** in the form of Criteria Strings (e.g. OrderDate \> '12/31/1999') affect the contents of a persisted **Recordset**.</span></span> <span data-ttu-id="fd9d9-154">**Filters** criados com uma Matriz de **Bookmarks** ou usando um valor de **FilterGroupEnum** não afetarão o conteúdo de um Recordset persistente.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-154">**Filters** created with an Array of **Bookmarks** or using a value from the **FilterGroupEnum** will not affect the contents of the persisted Recordset.</span></span> <span data-ttu-id="fd9d9-155">Essas regras aplicam-se a **Recordsets** criados com cursores do lado do cliente e do servidor.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-155">These rules apply to **Recordsets** created with either client-side or server-side cursors.</span></span>


> [!NOTE]
> <P><span data-ttu-id="fd9d9-p110">[!OBSERVAçãO] Quando você aplica o sinalizador <STRONG>adFilterPendingRecords</STRONG> a um <STRONG>Recordset</STRONG> filtrado e modificado no modo de atualização em lote, o <STRONG>Recordset</STRONG> resultante será vazio se a filtragem tiver sido baseada no campo de chave de uma tabela de chave única e a modificação tiver sido feita nos valores do campo de chave. O <STRONG>Recordset</STRONG> resultante não será vazio se uma das afirmações a seguir for verdadeira:</span><span class="sxs-lookup"><span data-stu-id="fd9d9-p110">When you apply the <STRONG>adFilterPendingRecords</STRONG> flag to a filtered and modified <STRONG>Recordset</STRONG> in the batch update mode, the resultant <STRONG>Recordset</STRONG> is empty if the filtering was based on the key field of a single-keyed table and the modification was made on the key field values. The resultant <STRONG>Recordset</STRONG> will be non-empty if one of the following is true:</span></span></P>



  - <span data-ttu-id="fd9d9-158">A filtragem foi baseada em campos sem chave, em uma tabela de chave única.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-158">The filtering was based on non-key fields in a single-keyed table.</span></span>

  - <span data-ttu-id="fd9d9-159">A filtragem foi baseada em qualquer campo, em uma tabela de várias chaves.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-159">The filtering was based on any fields in a multiple-keyed table.</span></span>

  - <span data-ttu-id="fd9d9-160">As modificações foram feitas em campos sem chave, em uma tabela de chave única.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-160">Modifications were made on non-key fields in a single-keyed table.</span></span>

  - <span data-ttu-id="fd9d9-161">As modificações foram feitas em qualquer campo, em uma tabela de várias chaves.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-161">Modifications were made on any fields in a multiple-keyed table.</span></span>

<span data-ttu-id="fd9d9-p111">A tabela a seguir resume os efeitos de **adFilterPendingRecords** em diferentes combinações de filtragem e modificações. A coluna da esquerda mostra as possíveis modificações; as modificações podem ser feitas em qualquer campo sem chave, no campo de chave em uma tabela de chave única ou em qualquer campo de chave em uma tabela de várias chaves. A linha superior mostra o critério de filtragem; a filtragem pode se basear em qualquer campo sem chaves, no campo de chave em uma tabela de chave única ou em qualquer campo de chave em uma tabela de várias chaves. As células de interseção mostram os resultados: + significa que aplicar **adFilterPendingRecords** resulta em um **Recordset** não vazio; **-** significa um **Recordset** vazio.</span><span class="sxs-lookup"><span data-stu-id="fd9d9-p111">The following table summarizes the effects of **adFilterPendingRecords** in different combinations of filtering and modifications. The left column shows the possible modifications; modifications can be made on any of the non-keyed fields, on the key field in a single-keyed table, or on any of the key fields in a multiple-keyed table. The top row shows the filtering criterion; filtering can be based on any of the non-keyed fields, the key field in a single-keyed table, or any of the key fields in a multiple-keyed table. The intersecting cells show the results: + means that applying **adFilterPendingRecords** results in a non-empty **Recordset**; **-** means an empty **Recordset**.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
</p></th>
<th><p><span data-ttu-id="fd9d9-166">Sem chaves</span><span class="sxs-lookup"><span data-stu-id="fd9d9-166">Non keys</span></span></p></th>
<th><p><span data-ttu-id="fd9d9-167">Chave única</span><span class="sxs-lookup"><span data-stu-id="fd9d9-167">Single Key</span></span></p></th>
<th><p><span data-ttu-id="fd9d9-168">Várias chaves</span><span class="sxs-lookup"><span data-stu-id="fd9d9-168">Multiple Keys</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fd9d9-169">Sem chaves</span><span class="sxs-lookup"><span data-stu-id="fd9d9-169">Non keys</span></span></p></td>
<td><p>+</p></td>
<td><p>+</p></td>
<td><p>+</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fd9d9-170">Chave única</span><span class="sxs-lookup"><span data-stu-id="fd9d9-170">Single Key</span></span></p></td>
<td><p>+</p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="fd9d9-171">N/D</span><span class="sxs-lookup"><span data-stu-id="fd9d9-171">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fd9d9-172">Várias chaves</span><span class="sxs-lookup"><span data-stu-id="fd9d9-172">Multiple Keys</span></span></p></td>
<td><p>+</p></td>
<td><p><span data-ttu-id="fd9d9-173">N/A</span><span class="sxs-lookup"><span data-stu-id="fd9d9-173">N/A</span></span></p></td>
<td><p>+</p></td>
</tr>
</tbody>
</table>

