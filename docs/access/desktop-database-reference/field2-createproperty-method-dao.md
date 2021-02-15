---
title: Método Field2.CreateProperty (DAO)
TOCTitle: CreateProperty Method
ms:assetid: bdbd6bec-216f-138e-78df-9c3221692aa4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822737(v=office.15)
ms:contentKeyID: 48547446
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf35138a4782e1f16d230ba120bf5482a9a8ce40
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292843"
---
# <a name="field2createproperty-method-dao"></a>Método Field2.CreateProperty (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Cria um novo objeto **[Property](property-object-dao.md)** definido pelo usuário (apenas espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)

*expressão* Uma variável que representa um objeto **Field2**.

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
<th><p>Necessária/opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variantes</strong></p></td>
<td><p>Uma <strong>String</strong> que denomina exclusivamente o novo objeto <strong>Property</strong>. Consulte a propriedade <strong>Name</strong> para obter detalhes sobre nomes válidos de <strong>Property</strong>.</p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variantes</strong></p></td>
<td><p>Uma constante que define o tipo de dados do novo objeto <strong>Property</strong>. Consulte a propriedade <strong><a href="field-type-property-dao.md">Type</a></strong> para obter tipos de dados válidos.</p></td>
</tr>
<tr class="odd">
<td><p><em>Value</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variantes</strong></p></td>
<td><p>Um <strong>Variant</strong> que contém o valor inicial da propriedade. Consulte a <strong><a href="field-value-property-dao.md">propriedade Value</a></strong> para obter detalhes.</p></td>
</tr>
<tr class="even">
<td><p><em>DDL</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variantes</strong></p></td>
<td><p>Um <strong>Variant</strong> (subtipo <strong>Boolean</strong>) que indica se <strong>Property</strong> é ou não um objeto DDL. O padrão é <strong>False</strong>. Se DDL for <strong>True</strong>, os usuários não poderão alterar ou excluir esse objeto <strong>Property,</strong> a menos que tenham <strong>permissão dbSecWriteDef.</strong></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valor de retorno

Propriedade

## <a name="remarks"></a>Comentários

Você pode criar um objeto **Property** definido pelo usuário na coleção **[Properties](properties-collection-dao.md)** de um objeto que é persistente.

Se você omitir uma ou mais das partes opcionais ao utilizar **CreateProperty**, poderá usar uma instruções de atribuição apropriada para definir ou redefinir a propriedade correspondente antes de acrescentar o novo objeto a uma coleção. Depois de acrescentar o objeto, você poderá alterar algumas, mas não todas, as configurações de propriedade. Consulte os tópicos de propriedade **Name**, **Type** e **Value** para obter mais detalhes.

Se o nome se referir a um objeto que já é membro da coleção, ocorrerá um erro em tempo de executar quando você usar o **[método Append.](fields-append-method-dao.md)**

Para remover um objeto **Property** definido pelo usuário da coleção, use o método **[Delete](fields-delete-method-dao.md)** na coleção **[Properties](properties-collection-dao.md)**. Não é possível excluir propriedades internas.


> [!NOTE]
> Se você omitir o argumento DDL, ele será o padrão para False (não-DDL). Como nenhuma propriedade DDL correspondente está exposta, você deve excluir e recriar o objeto **Property** que deseja alterar de DDL para não-DDL.


