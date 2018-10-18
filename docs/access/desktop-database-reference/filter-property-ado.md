---
<<<<<<< Título cabeça: propriedade Filter (ADO) TOCTitle: propriedade Filter (ADO) === título: propriedade Filter (ADO) TOCTitle: propriedade Filter (ADO)
>>>>>>> ms:assetid de mestre: 5abc528a-a6ee-34de-5d44-a3249194b0a0 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249314(v=office.15) ms:contentKeyID: ms.date 48545053: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="filter-property-ado"></a>Propriedade Filter (ADO)
=======
# <a name="filter-property-ado"></a>Propriedade Filter (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica um filtro para os dados em um [Recordset](recordset-object-ado.md).

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna um valor **Variant**, que pode conter:

  - **Sequência de critérios**  uma cadeia de caracteres formada por uma ou mais cláusulas individuais concatenadas com os operadores **AND** ou **OR**.

  - **Matriz de indicadores**  uma matriz de valores de indicadores exclusivos que apontam para registros no objeto **Recordset**.

  - Um valor [FilterGroupEnum](filtergroupenum.md).

## <a name="remarks"></a>Comentários

Use a propriedade **Filter** para filtrar de maneira seletiva os registros de um objeto **Recordset**. O **Recordset** filtrado torna-se o cursor atual. Outras propriedades que retornam valores com base no cursor atual são afetadas, como [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), [RecordCount](recordcount-property-ado.md) e [PageCount](pagecount-property-ado.md). Isso ocorre porque definir a propriedade **Filter** para um valor específico moverá o registro atual para o primeiro registro que atende ao novo valor.

A sequência de critérios é formada por cláusulas no formulário *FieldName-Operator-Value* (por exemplo, "LastName = 'Smith'"). Você pode criar cláusulas compostas concatenando cláusulas individuais com **AND** (por exemplo, "LastName = 'Smith' e FirstName = 'John'") ou **OR** (por exemplo, "). Você pode criar cláusulas compostas concatenando cláusulas individuais com **AND** (por exemplo, "LastName = 'Smith' e FirstName = 'John'") ou **OR** (por exemplo, "LastName = 'Smith' ou LastName = 'Jones'"). Use as seguintes diretrizes para as sequências de critérios:

  - *FieldName* deve ser um nome de campo válido do **Recordset**. Se o nome do campo contiver espaços, você deverá colocar o nome entre colchetes.

  - *Operator* deve ser um dos seguintes: \<, \>, \<=, \>=, \< \>, inglês, ou **como**.

  - *É o valor com o qual você irá comparar os valores de campo* (por exemplo, 'Smith', \#8/24/95\#, 12.345 ou US $50,00). Usar aspas simples com cadeias de caracteres e sinais numéricos (\#) com datas. Para os números, você pode usar casas decimais, sinais de dólar e notação científica. Se o *operador* é **SEMELHANTE**, o *valor* pode usar caracteres curinga. Somente o asterisco (\*) e o sinal de porcentagem (%) caracteres curinga é permitida, e eles devem ser o último caractere na cadeia de caracteres. *Valor* não pode ser nulo.
    

    > [!NOTE]
    > <P>[!OBSERVAçãO] Para incluir aspas simples (') no filtro Value, use duas aspas simples para representar uma. Por exemplo, para filtrar em O'Malley, a sequência de critérios deve ser "col1 = 'O''Malley'". Para incluir aspas simples no início e no final do valor de filtragem, coloque a sequência entre símbolos de libra (#). Por exemplo, para filtrar em '1', a sequência de critérios deve ser "col1 = #'1'#".</P>



  - Não há precedência entre **AND** e **OR**. As cláusulas podem ser agrupadas entre parênteses. No entanto, não é possível agrupar as cláusulas unidas por um **OR** e, em seguida, unir o grupo a outra cláusula com um **AND**, como neste exemplo:

  - Em vez disso, você deve construir esse filtro como

  - Em uma cláusula **LIKE** , você pode usar um curinga no início e no final do padrão (por exemplo, LastName Like '\*mit\*'), ou apenas no final do padrão (por exemplo, LastName Like ' Smit\*').

As constantes de filtragem tornam mais fácil resolver conflitos individuais de registro durante o modo de atualização em lote, permitindo que você exiba, por exemplo, apenas os registros que foram afetados durante a última chamada do método [UpdateBatch](updatebatch-method-ado.md).

A definição da propriedade **Filter** pode falhar devido a um conflito com os dados de base (por exemplo, um registro já foi excluído por outro usuário). Nesse caso, o provedorretorna avisos para a coleção [Errors](errors-collection-ado.md), mas não paralisa a execução do programa. Um erro de tempo de execução ocorre apenas quando houver conflitos em todos os registros solicitados. Use a propriedade [Status](status-property-ado-recordset.md) para localizar registros com conflitos.

Definir a propriedade **Filter** para uma sequência de comprimento zero ("") tem o mesmo efeito que usar a constante **adFilterNone**.

Sempre que a propriedade **Filter** for definida, a posição atual do registro passará para o primeiro registro no subconjunto filtrado de registros no **Recordset**. Da mesma forma, quando a propriedade **Filter** estiver em branco, a posição atual do registro passará para o primeiro registro no **Recordset**.

Consulte a propriedade [Bookmark](bookmark-property-ado.md) para obter uma explicação sobre valores de indicadores a partir dos quais é possível construir uma matriz para usar com a propriedade **Filter**.

Somente os **filtros** no formato de cadeias de caracteres de critérios (ex.: DataDoPedido \> ' 12/31/1999 ') afetam o conteúdo de um **Recordset**de persistido. **Filters** criados com uma Matriz de **Bookmarks** ou usando um valor de **FilterGroupEnum** não afetarão o conteúdo de um Recordset persistente. Essas regras aplicam-se a **Recordsets** criados com cursores do lado do cliente e do servidor.


> [!NOTE]
> <P>[!OBSERVAçãO] Quando você aplica o sinalizador <STRONG>adFilterPendingRecords</STRONG> a um <STRONG>Recordset</STRONG> filtrado e modificado no modo de atualização em lote, o <STRONG>Recordset</STRONG> resultante será vazio se a filtragem tiver sido baseada no campo de chave de uma tabela de chave única e a modificação tiver sido feita nos valores do campo de chave. O <STRONG>Recordset</STRONG> resultante não será vazio se uma das afirmações a seguir for verdadeira:</P>



  - A filtragem foi baseada em campos sem chave, em uma tabela de chave única.

  - A filtragem foi baseada em qualquer campo, em uma tabela de várias chaves.

  - As modificações foram feitas em campos sem chave, em uma tabela de chave única.

  - As modificações foram feitas em qualquer campo, em uma tabela de várias chaves.

A tabela a seguir resume os efeitos de **adFilterPendingRecords** em diferentes combinações de filtragem e modificações. A coluna da esquerda mostra as possíveis modificações; as modificações podem ser feitas em qualquer campo sem chave, no campo de chave em uma tabela de chave única ou em qualquer campo de chave em uma tabela de várias chaves. A linha superior mostra o critério de filtragem; a filtragem pode se basear em qualquer campo sem chaves, no campo de chave em uma tabela de chave única ou em qualquer campo de chave em uma tabela de várias chaves. As células de interseção mostram os resultados: + significa que aplicar **adFilterPendingRecords** resulta em um **Recordset** não vazio; **-** significa um **Recordset** vazio.

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
<th><p>Sem chaves</p></th>
<th><p>Chave única</p></th>
<th><p>Várias chaves</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Sem chaves</p></td>
<td><p>+</p></td>
<td><p>+</p></td>
<td><p>+</p></td>
</tr>
<tr class="even">
<td><p>Chave única</p></td>
<td><p>+</p></td>
<td><p>-</p></td>
<td><p>N/D</p></td>
</tr>
<tr class="odd">
<td><p>Várias chaves</p></td>
<td><p>+</p></td>
<td><p>N/A</p></td>
<td><p>+</p></td>
</tr>
</tbody>
</table>

