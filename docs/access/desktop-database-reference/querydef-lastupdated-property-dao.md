---
title: Propriedade QueryDef.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 98bb600e6f3f1c9587eca110269e8b6b3765e40f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921268"
---
# <a name="querydeflastupdated-property-dao"></a><span data-ttu-id="a1cb8-102">Propriedade QueryDef.LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="a1cb8-102">QueryDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="a1cb8-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1cb8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1cb8-p101">Retorna a data e a hora da alteração feita mais recentemente em um objeto. **Variant** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a1cb8-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1cb8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1cb8-106">Syntax</span></span>

<span data-ttu-id="a1cb8-107">*expressão* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="a1cb8-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="a1cb8-108">*expressão* Uma variável que representa um objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="a1cb8-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1cb8-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1cb8-109">Remarks</span></span>

<span data-ttu-id="a1cb8-p102">**DateCreated** e **LastUpdated** retornam a data e a hora em que o objeto foi criado ou atualizado pela última vez. Em um ambiente de vários usuários, os usuários devem obter essas configurações diretamente do servidor de arquivos para evitar discrepâncias nas configurações das propriedades DateCreated e LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="a1cb8-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

