---
title: Propriedade TableDef.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 994543132fb5323566bd876da066419d0986bd91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308411"
---
# <a name="tabledeflastupdated-property-dao"></a><span data-ttu-id="23de8-102">Propriedade TableDef.LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="23de8-102">TableDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="23de8-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="23de8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23de8-104">Retorna a data e a hora da alteração mais recente feita em um objeto.</span><span class="sxs-lookup"><span data-stu-id="23de8-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="23de8-105">**Variant** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="23de8-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="23de8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23de8-106">Syntax</span></span>

<span data-ttu-id="23de8-107">*expressão* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="23de8-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="23de8-108">*expressão* Uma variável que representa um objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="23de8-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="23de8-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="23de8-109">Remarks</span></span>

<span data-ttu-id="23de8-p102">**DateCreated** e **LastUpdated** retornam a data e a hora nas quais o objeto foi criado ou atualizado pela última vez. Em um ambiente multiusuário, os usuários devem obter essas definições diretamente do servidor de arquivos para evitar discrepâncias nas definições das propriedades DateCreated e LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="23de8-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

