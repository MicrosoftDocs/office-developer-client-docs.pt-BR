---
title: Propriedade TableDef.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3840ef8b2a01f28bd2a9881848c813f85411fb7b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464032"
---
# <a name="tabledeflastupdated-property-dao"></a><span data-ttu-id="ad5dd-102">Propriedade TableDef.LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="ad5dd-102">TableDef.LastUpdated Property (DAO)</span></span>


<span data-ttu-id="ad5dd-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad5dd-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ad5dd-p101">Retorna a data e a hora da alteração feita mais recentemente em um objeto. **Variant** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="ad5dd-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad5dd-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad5dd-106">Syntax</span></span>

<span data-ttu-id="ad5dd-107">*expressão* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="ad5dd-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="ad5dd-108">*expressão* Uma variável que representa um objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="ad5dd-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad5dd-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad5dd-109">Remarks</span></span>

<span data-ttu-id="ad5dd-p102">**DateCreated** e **LastUpdated** retornam a data e a hora em que o objeto foi criado ou atualizado pela última vez. Em um ambiente de vários usuários, os usuários devem obter essas configurações diretamente do servidor de arquivos para evitar discrepâncias nas configurações das propriedades DateCreated e LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="ad5dd-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

