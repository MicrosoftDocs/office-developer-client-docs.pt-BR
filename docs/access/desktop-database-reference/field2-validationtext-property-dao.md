---
title: Propriedade Field2.ValidationText (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6128f66c-3891-ae4d-d12d-354a79a9c05e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194867(v=office.15)
ms:contentKeyID: 48545202
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b8ce99f7fbedc487f5c5bae98745f1d446c2da3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25867143"
---
# <a name="field2validationtext-property-dao"></a><span data-ttu-id="5ff6d-102">Propriedade Field2.ValidationText (DAO)</span><span class="sxs-lookup"><span data-stu-id="5ff6d-102">Field2.ValidationText Property (DAO)</span></span>


<span data-ttu-id="5ff6d-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="5ff6d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5ff6d-p101">Define ou retorna um valor que especifica o texto da mensagem que o aplicativo exibe se o valor de um objeto **Field2** não atende à regra de validação especificada pela configuração da propriedade **ValidationRule** (apenas espaços de trabalho do Microsoft Access). **String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-p101">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field2** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ff6d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ff6d-106">Syntax</span></span>

<span data-ttu-id="5ff6d-107">*expressão* . ValidationText</span><span class="sxs-lookup"><span data-stu-id="5ff6d-107">*expression* .ValidationText</span></span>

<span data-ttu-id="5ff6d-108">*expressão* Uma variável que representa um objeto **Field2** .</span><span class="sxs-lookup"><span data-stu-id="5ff6d-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ff6d-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ff6d-109">Remarks</span></span>

<span data-ttu-id="5ff6d-p102">O valor de configuração ou de retorno é uma **String** que especifica o texto exibido se um usuário tenta digitar um valor inválido em um campo. Para um objeto que não está acrescentado a uma coleção, essa propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-p102">The setting or return value is a **String** that specifies the text displayed if a user tries to enter an invalid value for a field. For an object not yet appended to a collection, this property is read/write.</span></span>

<span data-ttu-id="5ff6d-112">Para um objeto **Field2**, a utilização da propriedade **ValidationText** depende do objeto que contém a coleção **[Fields](fields-collection-dao.md)** à qual o objeto **Field2** foi acrescentado, como mostra a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5ff6d-112">For a **Field2** object, use of the **ValidationText** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection to which the **Field2** object is appended, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5ff6d-113">Objeto acrescentado a</span><span class="sxs-lookup"><span data-stu-id="5ff6d-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="5ff6d-114">Uso</span><span class="sxs-lookup"><span data-stu-id="5ff6d-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ff6d-115"><strong>Índice</strong></span><span class="sxs-lookup"><span data-stu-id="5ff6d-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="5ff6d-116">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="5ff6d-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ff6d-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="5ff6d-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="5ff6d-118">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ff6d-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ff6d-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="5ff6d-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="5ff6d-120">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ff6d-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ff6d-121"><strong>Relação</strong></span><span class="sxs-lookup"><span data-stu-id="5ff6d-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="5ff6d-122">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="5ff6d-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ff6d-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="5ff6d-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="5ff6d-124">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5ff6d-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

