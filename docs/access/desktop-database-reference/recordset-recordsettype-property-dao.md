---
title: Propriedade Recordset. RecordsetType (DAO)
TOCTitle: RecordsetType Property
ms:assetid: a66d4043-08cc-ead1-f9ff-efc7d7ea21bf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821178(v=office.15)
ms:contentKeyID: 48546853
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13361
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 64f7dda8bec7806ef510d265deab350dc3cdad6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307627"
---
# <a name="recordsetrecordsettype-property-dao"></a>Propriedade Recordset. RecordsetType (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Você pode utilizar a propriedade **RecordsetType** para especificar o tipo de conjunto de registros que estará disponível para um formulário. **Byte** de leitura/gravação.

## <a name="syntax"></a>Sintaxe

*expressão* . RecordsetType

*expression* Uma variável que representa um objeto **Form**.

## <a name="remarks"></a>Comentários

A propriedade **RecordsetType** utiliza as configurações a seguir em um banco de dados do Microsoft Access.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Configuração</p></th>
<th><p>Tipo de conjunto de registros</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>,0</p></td>
<td><p>Aceita</p></td>
<td><p>(Padrão) Você pode editar controles ligados com base em uma única tabela ou em tabelas com uma relação um-para-um. Para controles acoplados a campos baseados em tabelas com uma relação um-para-muitos, você não pode editar dados do campo de associação &quot;no&quot; lado único da relação, a menos que a atualização em cascata esteja habilitada entre as tabelas.</p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
<td><p>Dynaset (Atualizações inconsistentes)</p></td>
<td><p>Todas as tabelas e os controles ligados aos respectivos campos podem ser editados.</p></td>
</tr>
<tr class="odd">
<td><p>duas</p></td>
<td><p>Lo</p></td>
<td><p>Não é possível editar as tabelas nem os controles ligados aos respectivos campos.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!OBSERVAçãO] Se não desejar que dados em controles ligados sejam editados quando um formulário estiver no modo Formulário ou no modo Folha de Dados, você poderá definir a propriedade **RecordsetType** como 2.

A propriedade **RecordsetType** utiliza as configurações a seguir em um projeto do Microsoft Access (.adp).

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Configuração</p></th>
<th><p>Tipo de conjunto de registros</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>3D</p></td>
<td><p>Lo</p></td>
<td><p>Não é possível editar as tabelas nem os controles ligados aos respectivos campos.</p></td>
</tr>
<tr class="even">
<td><p>quatro</p></td>
<td><p>Instantâneo atualizável</p></td>
<td><p>(Padrão) Todas as tabelas e os controles ligados aos respectivos campos podem ser editados.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!OBSERVAçãO] Alterar a propriedade **RecordsetType** de um formulário ou de um relatório aberto resulta na recriação automática do conjunto de registros.

Você pode criar formulários com base em várias tabelas base com campos ligados a controles nos formulários. Dependendo da configuração da propriedade **RecordsetType**, você poderá limitar os controles ligados a serem editados.

Além do controle de edição fornecido pelo **RecordsetType**, cada controle em um formulário tem uma propriedade **Locked** que você pode definir para especificar se o controle e seus dados subjacentes podem ser editados. Se a propriedade **Locked** estiver definida como Sim, você não poderá editar os dados.

## <a name="example"></a>Exemplo

No exemplo a seguir, os registros somente poderão ser atualizados se a identificação do usuário for ADMIN. Este exemplo de código definirá a propriedade **RecordsetType** como Snapshot se o valor gstrUserID da variável pública for diferente de ADMIN.

```vb
    Sub Form_Open(Cancel As Integer) 
     Const conSnapshot = 2 
     If gstrUserID <> "ADMIN" Then 
     Forms!Employees.RecordsetType = conSnapshot 
     End If 
    End Sub
```

## <a name="see-also"></a>Confira também

- [Objeto Form](https://docs.microsoft.com/office/vba/api/Access.Form)


