---
title: Propriedade TableDef.ReplicaFilter (DAO)
TOCTitle: ReplicaFilter Property
ms:assetid: f44273de-2b6a-750f-cb7c-12c3ac2da503
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836681(v=office.15)
ms:contentKeyID: 48548683
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055548
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 5104aa452dfc8bc73c378c30a454f676d455c9f1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464725"
---
# <a name="tabledefreplicafilter-property-dao"></a>Propriedade TableDef.ReplicaFilter (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Define ou retorna um valor em um objeto **[TableDef](tabledef-object-dao.md)** em uma réplica parcial que indica qual subconjunto de registros foi replicado nessa tabela a partir de uma réplica completa. (Somente em espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . ReplicaFilter

*expressão* Uma variável que representa um objeto **TableDef** .

## <a name="remarks"></a>Comentários

A configuração ou o valor de retorno é um **String** ou **Boolean** que indica qual subconjunto de registros foi replicado, conforme especificado na tabela a seguir:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valor</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>String</p></td>
<td><p>Os critérios aos quais um registro em uma tabela de réplicas parciais deve atender para ser replicado a partir de uma réplica completa.</p></td>
</tr>
<tr class="even">
<td><p><strong>True</strong></p></td>
<td><p>Replica todos os registros.</p></td>
</tr>
<tr class="odd">
<td><p><strong>False</strong></p></td>
<td><p>(Padrão) Não replica registros.</p></td>
</tr>
</tbody>
</table>


Essa propriedade é semelhante à cláusula SQL WHERE (sem a palavra WHERE), mas não será possível especificar subconsultas, funções agregadas (como **Count**) ou funções definidas pelo usuário dentro dos critérios.

Você pode sincronizar os dados apenas entre uma réplica completa e uma réplica parcial. Não é possível sincronizar dados entre duas réplicas parciais. Além disso, com uma replicação parcial, você pode definir as restrições nos registros que serão replicados, mas não pode indicar quais campos serão replicados.

Geralmente, você redefinirá um filtro para réplica quando quiser replicar um conjunto de registros diferentes. Por exemplo, quando um representante de vendas assumir temporariamente o controle da região de outros representantes de vendas, o aplicativo do banco de dados poderá replicar temporariamente os dados de ambas as regiões e mais tarde retornar para o filtro anterior. Neste cenário, o aplicativo redefinirá a propriedade **ReplicaFilter** e depois preencherá novamente a réplica parcial.

Se o aplicativo alterar os filtros das réplicas, você deverá seguir estas etapas:

1.  Use o método **[Synchronize](database-synchronize-method-dao.md)** para sincronizar a réplica completa com a réplica parcial a partir da qual os filtros estão sendo alterados.

2.  Use a propriedade **ReplicaFilter** para fazer as alterações desejadas no filtro para réplica.

3.  Use o método **[PopulatePartial](database-populatepartial-method-dao.md)** para remover todos os registros da réplica parcial e transferir todos os registros da réplica completa que correspondem aos novos critérios do filtro para réplica.

Para remover um filtro, defina a propriedade **ReplicaFilter** como **False**. Se você remover todos os filtros e chamar o método **PopulatePartial**, nenhum registro aparecerá nas tabelas replicadas da réplica parcial.


> [!NOTE]
> <P>[!OBSERVAçãO] Se um filtro para réplica foi alterado e o método <STRONG>Synchronize</STRONG> for chamado antes do método <STRONG>PopulatePartial</STRONG>, ocorrerá um erro interceptável.</P>



## <a name="example"></a>Exemplo

O exemplo a seguir usa a propriedade **ReplicaFilter** para replicar somente os registros dos clientes da região da Califórnia.

```vb 
Sub ReplicaFilterX() 
 
 ' This example assumes the current open database 
 ' is the replica. 
 Dim tdfCustomers As TableDef 
 Dim strFilter As String 
 Dim dbsTemp As Database 
 
 Set dbsTemp = OpenDatabase("Northwind.mdb") 
 Set tdfCustomers = dbsTemp.TableDefs("Customers") 
 
 ' Synchronize with full replica 
 ' before setting replica filter. 
 dbsTemp.Synchronize "C:\SALES\FY96.MDB" 
 
 strFilter = "Region = 'CA'" 
 tdfCustomers.ReplicaFilter = strFilter 
 dbsTemp.PopulatePartial "C:\SALES\FY96.MDB" 
 
 ' Now remove the replica filter (for example purposes 
 ' only). 
 tdfCustomers.ReplicaFilter = False 
 ' Repopulate the database. 
 dbsTemp.PopulatePartial "C:\SALES\DATA96.MDB" 
 
End Sub 
 
```
