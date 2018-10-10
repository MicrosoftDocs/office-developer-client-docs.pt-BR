---
title: Propriedade QueryDef.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 37a95cefb5af5070470fb5973076e230d76c3d98
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465362"
---
# <a name="querydeflastupdated-property-dao"></a><span data-ttu-id="ede2e-102">Propriedade QueryDef.LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="ede2e-102">QueryDef.LastUpdated Property (DAO)</span></span>


<span data-ttu-id="ede2e-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ede2e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ede2e-p101">Retorna a data e a hora da alteração feita mais recentemente em um objeto. **Variant** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="ede2e-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ede2e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ede2e-106">Syntax</span></span>

<span data-ttu-id="ede2e-107">*expressão* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="ede2e-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="ede2e-108">*expressão* Uma variável que representa um objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="ede2e-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ede2e-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="ede2e-109">Remarks</span></span>

<span data-ttu-id="ede2e-p102">**DateCreated** e **LastUpdated** retornam a data e a hora em que o objeto foi criado ou atualizado pela última vez. Em um ambiente de vários usuários, os usuários devem obter essas configurações diretamente do servidor de arquivos para evitar discrepâncias nas configurações das propriedades DateCreated e LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="ede2e-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

