---
title: Propriedade Relations.Count (DAO)
TOCTitle: Count Property
ms:assetid: 7cb3885f-6896-8402-8b18-12769473f051
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196377(v=office.15)
ms:contentKeyID: 48545843
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c1be0766c1f1a2057e5cb7137d2e9131a2505f75
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876005"
---
# <a name="relationscount-property-dao"></a><span data-ttu-id="344d9-102">Propriedade Relations.Count (DAO)</span><span class="sxs-lookup"><span data-stu-id="344d9-102">Relations.Count Property (DAO)</span></span>


<span data-ttu-id="344d9-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="344d9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="344d9-p101">Retorna o número de objetos na coleção especificada. Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="344d9-p101">Returns the number of objects in the specified collection. Read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="344d9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="344d9-106">Syntax</span></span>

<span data-ttu-id="344d9-107">*expressão* . Contagem</span><span class="sxs-lookup"><span data-stu-id="344d9-107">*expression* .Count</span></span>

<span data-ttu-id="344d9-108">*expressão* Uma variável que representa um objeto **Relations** .</span><span class="sxs-lookup"><span data-stu-id="344d9-108">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="344d9-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="344d9-109">Remarks</span></span>

<span data-ttu-id="344d9-p102">Como os membros de uma coleção começam com 0, você sempre deve codificar os loops começando com o membro 0 e terminando com o valor da propriedade **Count** menos 1. Para efetuar loop pelos membros de uma coleção sem verificar a propriedade **Count**, use o comando **For Each...Next**.</span><span class="sxs-lookup"><span data-stu-id="344d9-p102">Because members of a collection begin with 0, you should always code loops starting with the 0 member and ending with the value of the **Count** property minus 1. If you want to loop through the members of a collection without checking the **Count** property, you can use a **For Each...Next** command.</span></span>

<span data-ttu-id="344d9-p103">A definição da propriedade **Count** nunca será Null. Se o valor for 0, não haverá objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="344d9-p103">The **Count** property setting is never Null. If its value is 0, there are no objects in the collection.</span></span>

