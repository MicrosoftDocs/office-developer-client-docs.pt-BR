---
title: Método Database.PopulatePartial (DAO)
TOCTitle: PopulatePartial Method
ms:assetid: fa3227a2-c961-6a98-32b3-5b6e5329a21d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837034(v=office.15)
ms:contentKeyID: 48548834
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101186
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9e0f77c356e0a13c2a1a83986a92c2b25029ecb4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709919"
---
# <a name="databasepopulatepartial-method-dao"></a>Método Database.PopulatePartial (DAO)

**Aplica-se a**: Access 2013, o Office 2013

Sincroniza as alterações em uma réplica parcial com a réplica completa, limpa todos os registros na réplica parcial e preenche novamente a réplica parcial com base nos filtros da réplica atual. (Apenas bancos de dados do mecanismo de banco de dados do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . PopulatePartial (***DbPathName***)

*expressão* Uma variável que representa um objeto de **banco de dados** .

## <a name="parameters"></a>Parâmetros

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Obrigatório/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>DbPathName</em></p></td>
<td><p>Obrigatório</p></td>
<td><p><strong>String</strong></p></td>
<td><p>O caminho e o nome da réplica completa a partir da qual os registros serão preenchidos.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentários

Quando você sincroniza uma réplica parcial com uma réplica completa, é possível criar registros "órfãos" na réplica parcial. Por exemplo, suponha que você tem uma tabela Customers com seu **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** definido como "região = 'CA'". Se um usuário alterar uma região de Customers de CA para NY na réplica parcial e, em seguida, ocorrer uma sincronização por meio do método **[Synchronize](database-synchronize-method-dao.md)**, a alteração será propagada para a réplica completa mas o registro que contém NY na réplica parcial é órfão porque agora ele não satisfaz aos critérios do filtro da réplica.

Para solucionar o problema dos registros órfãos, você pode usar o método **PopulatePartial**. O método **PopulatePartial** é semelhante ao método **Synchronize**, mas ele sincroniza quaisquer alterações com a réplica completa, remove todos os registros na réplica parcial e, em seguida, preenche novamente a réplica parcial com base nos atuais filtros da réplica. Mesmo que os filtros da réplica não tiverem sido alterados, **PopulatePartial** sempre limpará os registros na réplica parcial e os preencherá novamente com base nos filtros atuais.

Geralmente, você deve usar o método **PopulatePartial** ao criar uma réplica parcial e sempre que alterar os filtros da réplica. Se seu aplicativo alterar os filtros da réplica, você deve executar os seguintes procedimentos:

1.  Sincronize sua réplica completa com a réplica parcial nas quais os filtros estão sendo alterados.

2.  Use as propriedades **ReplicaFilter** e **[PartialReplica](relation-partialreplica-property-dao.md)** para fazer as alterações desejadas no filtro da réplica.

3.  Chame o método **PopulatePartial** para remover todos os registros da réplica parcial e transferir todos os registros da réplica completa que satisfazem os novos critérios do filtro da réplica.

Se um filtro de réplica tiver sido alterado e o método **Synchronize** for invocado sem que seja invocado primeiramente **PopulatePartial**, ocorrerá um erro interceptável.

O método **PopulatePartial** pode ser invocado apenas em uma réplica parcial que tiver sido aberta para acesso exclusivo. Além disso, não é possível chamar o método **PopulatePartial** a partir do código em execução dentro da própria réplica parcial. Em vez disso, abra a réplica parcial exclusivamente a partir da réplica completa ou de outro banco de dados e, em seguida, chame **PopulatePartial**.


> [!NOTE]
> [!OBSERVAçãO] Embora **PopulatePartial** execute uma sincronização de mão única antes de limpar e preencher novamente a réplica parcial, ainda é uma boa ideia chamar **Synchronize** antes de chamar **PopulatePartial**. Isso ocorre porque se a chamada de **Synchronize** falhar, ocorrerá um erro interceptável. Você pode usar esse erro para decidir prosseguir ou não com o método **PopulatePartial** (o que remove todos os registros da réplica parcial). Se **PopulatePartial** for chamado por si mesmo e ocorrer um erro enquanto os registros estiverem sendo sincronizados, os registros da réplica parcial ainda serão limpos, o que pode não ser o resultado desejado.



## <a name="example"></a>Exemplo

O exemplo a seguir usa o método **PopulatePartial** depois de alterar um filtro de réplica.

```vb 
Sub PopulatePartialX() 
 
 Dim tdfCustomers As TableDef 
 Dim strFilter As String 
 Dim dbsTemp As Database 
 
 ' Open the partial replica in exclusive mode. 
 Set dbsTemp = OpenDatabase("F:\SALES\FY96CA.MDB", True) 
 
 With dbsTemp 
 Set tdfCustomers = .TableDefs("Customers") 
 
 ' Synchronize with full replica 
 ' before setting replica filter. 
 .Synchronize "C:\SALES\FY96.MDB" 
 
 strFilter = "Region = 'CA'" 
 tdfCustomers.ReplicaFilter = strFilter 
 
 ' Populate records from the full replica. 
 .PopulatePartial "C:\SALES\FY96.MDB" 
 
 .Close 
 End With 
 
End Sub 
 
```

