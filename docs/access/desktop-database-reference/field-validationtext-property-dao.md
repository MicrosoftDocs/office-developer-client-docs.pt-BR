---
title: Propriedade Field.ValidationText (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6d9ec790-a9d2-84d7-ccba-57d738491e36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195540(v=office.15)
ms:contentKeyID: 48545494
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c582795dc104171bd4c8435521e0da31718b1a38
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868886"
---
# <a name="fieldvalidationtext-property-dao"></a><span data-ttu-id="4fbef-102">Propriedade Field.ValidationText (DAO)</span><span class="sxs-lookup"><span data-stu-id="4fbef-102">Field.ValidationText Property (DAO)</span></span>


<span data-ttu-id="4fbef-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="4fbef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4fbef-p101">Define ou retorna um valor que especifica o texto da mensagem exibido pelo aplicativo, caso o valor de um objeto **Field** não satisfaça a regra de validação especificada pela definição da propriedade **ValidationRule** (somente nos espaços de trabalho do Microsoft Access). **String** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4fbef-p101">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fbef-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4fbef-106">Syntax</span></span>

<span data-ttu-id="4fbef-107">*expressão* . ValidationText</span><span class="sxs-lookup"><span data-stu-id="4fbef-107">*expression* .ValidationText</span></span>

<span data-ttu-id="4fbef-108">*expressão* Uma variável que representa um objeto **Field** .</span><span class="sxs-lookup"><span data-stu-id="4fbef-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fbef-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="4fbef-109">Remarks</span></span>

<span data-ttu-id="4fbef-p102">O valor de definição ou de retorno é um **String** que especificará o texto exibido se um usuário tentar inserir um valor inválido em um campo. Para um objeto ainda não acrescentado a uma coleção, essa propriedade será leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4fbef-p102">The setting or return value is a **String** that specifies the text displayed if a user tries to enter an invalid value for a field. For an object not yet appended to a collection, this property is read/write.</span></span>

<span data-ttu-id="4fbef-112">Para um objeto **Field**, o uso da propriedade **ValidationText** depende do objeto que contém a coleção **[Fields](fields-collection-dao.md)** na qual o objeto **Field** foi acrescentado, como mostra a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4fbef-112">For a **Field** object, use of the **ValidationText** property depends on the object that contains the **[Fields](fields-collection-dao.md)** collection to which the **Field** object is appended, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4fbef-113">Objeto acrescentado a</span><span class="sxs-lookup"><span data-stu-id="4fbef-113">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="4fbef-114">Uso</span><span class="sxs-lookup"><span data-stu-id="4fbef-114">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4fbef-115"><strong>Índice</strong></span><span class="sxs-lookup"><span data-stu-id="4fbef-115"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="4fbef-116">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4fbef-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fbef-117"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="4fbef-117"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="4fbef-118">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4fbef-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fbef-119"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="4fbef-119"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="4fbef-120">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4fbef-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fbef-121"><strong>Relação</strong></span><span class="sxs-lookup"><span data-stu-id="4fbef-121"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="4fbef-122">Sem suporte</span><span class="sxs-lookup"><span data-stu-id="4fbef-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fbef-123"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="4fbef-123"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="4fbef-124">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="4fbef-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>

