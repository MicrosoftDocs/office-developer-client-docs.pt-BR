---
title: FieldEnum (referência de banco de dados da área de trabalho do Access)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 9ab46fc7c3817cbfa83c78816a42472e425d2d71
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860046"
---
# <a name="fieldenum"></a><span data-ttu-id="0dacf-102">FieldEnum</span><span class="sxs-lookup"><span data-stu-id="0dacf-102">FieldEnum</span></span>

<span data-ttu-id="0dacf-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0dacf-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0dacf-104">Especifica os campos especiais mencionados em uma coleção de [Campos](record-object-ado.md) do objeto [Record](fields-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0dacf-104">Specifies the special fields referenced in a [Record](record-object-ado.md) object's [Fields](fields-collection-ado.md) collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dacf-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="0dacf-105">Remarks</span></span>

<span data-ttu-id="0dacf-p101">Essas constantes fornecem um "atalho" para acessar os campos especiais associados a um **Record**. Recupere o objeto [Field](field-object-ado.md) da coleção de **Campos** e, em seguida, obtenha seu conteúdo com a propriedade **Value** do objeto [Field](value-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0dacf-p101">These constants provide a "shortcut" to accessing special fields associated with a **Record**. Retrieve the [Field](field-object-ado.md) object from the **Fields** collection, and then obtain its contents with the **Field** object's [Value](value-property-ado.md) property.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0dacf-108">Constant</span><span class="sxs-lookup"><span data-stu-id="0dacf-108">Constant</span></span></p></th>
<th><p><span data-ttu-id="0dacf-109">Valor</span><span class="sxs-lookup"><span data-stu-id="0dacf-109">Value</span></span></p></th>
<th><p><span data-ttu-id="0dacf-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="0dacf-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0dacf-111"><strong>adDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="0dacf-111"><strong>adDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="0dacf-112">-1</span><span class="sxs-lookup"><span data-stu-id="0dacf-112">-1</span></span></p></td>
<td><p><span data-ttu-id="0dacf-113">Faz referência ao campo que contém o objeto <a href="stream-object-ado.md">Stream</a> padrão associado a um <strong>Record</strong>.</span><span class="sxs-lookup"><span data-stu-id="0dacf-113">References the field containing the default <a href="stream-object-ado.md">Stream</a> object associated with a <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0dacf-114"><strong>adRecordURL</strong></span><span class="sxs-lookup"><span data-stu-id="0dacf-114"><strong>adRecordURL</strong></span></span></p></td>
<td><p><span data-ttu-id="0dacf-115">-2</span><span class="sxs-lookup"><span data-stu-id="0dacf-115">-2</span></span></p></td>
<td><p><span data-ttu-id="0dacf-116">Faz referência ao campo que contém a sequência de URL absoluto para o <strong>Record</strong> atual.</span><span class="sxs-lookup"><span data-stu-id="0dacf-116">References the field containing the absolute URL string for the current <strong>Record</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

