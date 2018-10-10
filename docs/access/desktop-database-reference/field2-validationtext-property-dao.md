---
title: Propriedade Field2.ValidationText (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6128f66c-3891-ae4d-d12d-354a79a9c05e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194867(v=office.15)
ms:contentKeyID: 48545202
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d971b14093dd02204327e6f0ef30a81c6567c5bc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465197"
---
# <a name="field2validationtext-property-dao"></a><span data-ttu-id="3f679-102">Propriedade Field2.ValidationText (DAO)</span><span class="sxs-lookup"><span data-stu-id="3f679-102">Field2.ValidationText Property (DAO)</span></span>


<span data-ttu-id="3f679-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f679-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3f679-p101">Define ou retorna um valor que especifica o texto da mensagem que o aplicativo exibe se o valor de um objeto **Field2** não atende à regra de validação especificada pela configuração da propriedade **ValidationRule** (apenas espaços de trabalho do Microsoft Access). **String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3f679-p101">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field2** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f679-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3f679-106">Syntax</span></span>

<span data-ttu-id="3f679-107">*expressão* . ValidationText</span><span class="sxs-lookup"><span data-stu-id="3f679-107">*expression* .ValidationText</span></span>

<span data-ttu-id="3f679-108">*expressão* Uma variável que representa um objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="3f679-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f679-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f679-109">Remarks</span></span>

<span data-ttu-id="3f679-p102">O valor de configuração ou de retorno é uma **String** que especifica o texto exibido se um usuário tenta digitar um valor inválido em um campo. Para um objeto que não está acrescentado a uma coleção, essa propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3f679-p102">The setting or return value is a **String** that specifies the text displayed if a user tries to enter an invalid value for a field. For an object not yet appended to a collection, this property is read/write.</span></span>

<span data-ttu-id="3f679-112">Para um objeto **Field2**, a utilização da propriedade **ValidationText** depende do objeto que contém a coleção **[Fields](fields-collection-dao.md)** à qual o objeto **Field2** foi acrescentado, como mostra a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3f679-112">For a **Field2** object, use of the **ValidationText** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection to which the **Field2** object is appended, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3f679-113">Objeto acrescentado a</span><span class="sxs-lookup"><span data-stu-id="3f679-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="3f679-114">Uso</span><span class="sxs-lookup"><span data-stu-id="3f679-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f679-115"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="3f679-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="3f679-116">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="3f679-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f679-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="3f679-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="3f679-118">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f679-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f679-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="3f679-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="3f679-120">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3f679-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3f679-121"><strong>Relação</strong></span><span class="sxs-lookup"><span data-stu-id="3f679-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="3f679-122">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="3f679-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3f679-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="3f679-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="3f679-124">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="3f679-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

