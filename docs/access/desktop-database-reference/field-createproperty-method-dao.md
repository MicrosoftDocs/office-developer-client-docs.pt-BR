---
title: Método Field.CreateProperty (DAO)
TOCTitle: CreateProperty Method
ms:assetid: b3c1d303-7cab-89c3-8e90-f18a0445d304
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822050(v=office.15)
ms:contentKeyID: 48547202
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: da540f657b1b5bc6cc5442588ea63c3ade72fd2b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25462634"
---
# <a name="fieldcreateproperty-method-dao"></a>Método Field.CreateProperty (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Cria um novo objeto **[Property](property-object-dao.md)** definido pelo usuário (somente espaços de trabalho do Microsoft Access).

## <a name="syntax"></a>Sintaxe

*expressão* . CreateProperty (***nome***, ***tipo***, ***valor***, ***DDL***)

*expressão* Uma variável que representa um objeto **Field** .

### <a name="parameters"></a>Parâmetros

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
<th><p>Obrigatório/Opcional</p></th>
<th><p>Tipo de dados</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Name</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma <strong>String</strong> que denomina exclusivamente o novo objeto <strong>Property</strong>. Consulte a propriedade <strong>Name</strong> para obter detalhes sobre nomes válidos de <strong>Property</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Tipo</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Uma constante que define o tipo de dados do novo objeto <strong>Property</strong>. Consulte a propriedade <strong><a href="field-type-property-dao.md">Type</a></strong> para obter tipos de dados válidos.</p></td>
</tr>
<tr class="odd">
<td><p>Valor</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Um <strong>Variant</strong> que contém o valor inicial da propriedade. Consulte a propriedade <strong><a href="field-value-property-dao.md">Value</a></strong> para obter detalhes.</p></td>
</tr>
<tr class="even">
<td><p>DDL</p></td>
<td><p>Opcional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Um <strong>Variant</strong> (subtipo<strong>booleano</strong> ) que indica se é ou não a <strong>propriedade</strong> de um objeto DDL. O padrão é <strong>False</strong>. Se DDL for <strong>True</strong>, os usuários não podem alterar ou excluir esse objeto de <strong>propriedade</strong> , a menos que tenham permissão <strong>dbSecWriteDef</strong> .</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valor retornado

Propriedade

## <a name="remarks"></a>Comentários

Você pode criar um objeto **Property** definido pelo usuário somente na coleção **[Properties](properties-collection-dao.md)** de um objeto que é persistente.

Se omitir uma ou mais dessas partes opcionais quando usar **CreateProperty**, você poderá usar uma instrução de atribuição apropriada para definir ou redefinir a propriedade correspondente antes de acrescentar o novo objeto à coleção. Depois de acrescentar o objeto, você poderá alterar algumas, mas não todas as configurações de propriedade. Consulte os tópicos de propriedade de **Name**, **Type** e **Value** para obter mais detalhes.

Se name fizer referência a um objeto que já é um membro da coleção, ocorrerá um erro de tempo de execução quando você usa o método **[Append](fields-append-method-dao.md)** .

Para remover um objeto **Property** definido pelo usuário da coleção, use o método **[Delete](fields-delete-method-dao.md)** na coleção **Properties**. Não é possível excluir propriedades internas.


> [!NOTE]
> <P>Se você omitir o argumento DDL, o padrão é False (não-DDL). Como nenhuma propriedade DDL correspondente está exposta, você deve excluir e recriar um objeto <STRONG>Property</STRONG> que deseja alterar de DDL para não-DDL.</P>


