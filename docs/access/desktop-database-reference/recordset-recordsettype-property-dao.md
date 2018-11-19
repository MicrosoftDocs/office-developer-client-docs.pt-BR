---
title: Propriedade Recordset.RecordsetType (DAO)
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
ms.openlocfilehash: e4babfce754ec0e9c4744142570054c0249936f8
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026208"
---
# <a name="recordsetrecordsettype-property-dao"></a>Propriedade Recordset.RecordsetType (DAO)

**Aplica-se a**: Access 2013, o Office 2013

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
<td><p>0</p></td>
<td><p>Dynaset</p></td>
<td><p>(Padrão) Você pode editar controles vinculados, com base em uma única tabela ou tabelas com um relacionamento individual. Para controles ligados aos campos baseados em tabelas com uma relação um-para-muitos, você não pode editar dados do campo de ingresso no &quot;um&quot; lado do relacionamento, a menos que propagar atualização está habilitada entre as tabelas.</p></td>
</tr>
<tr class="even">
<td><p>1</p></td>
<td><p>Dynaset (Atualizações inconsistentes)</p></td>
<td><p>Todas as tabelas e os controles ligados aos respectivos campos podem ser editados.</p></td>
</tr>
<tr class="odd">
<td><p>2</p></td>
<td><p>Instantâneo</p></td>
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
<td><p>3</p></td>
<td><p>Instantâneo</p></td>
<td><p>Não é possível editar as tabelas nem os controles ligados aos respectivos campos.</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p>Instantâneo atualizável</p></td>
<td><p>(Padrão) Todas as tabelas e os controles ligados aos respectivos campos podem ser editados.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!OBSERVAçãO] Alterar a propriedade **RecordsetType** de um formulário ou de um relatório aberto resulta na recriação automática do conjunto de registros.

Você pode criar formulários com base em várias tabelas base com campos ligados a controles nos formulários. Dependendo da configuração da propriedade **RecordsetType**, você poderá limitar os controles ligados a serem editados.

Além do controle de edição fornecido pelo **TipoDeConjuntoDeRegistros**, cada controle em um formulário tem uma propriedade **Locked** que você pode definir para especificar se o controle e seus dados base podem ser editados. Se a propriedade **Locked** estiver definida como Sim, você não poderá editar os dados.

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


