---
title: Propriedade QueryDef.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1876e92381828075edca3bbfcbae63e706a21365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303308"
---
# <a name="querydeflastupdated-property-dao"></a><span data-ttu-id="66594-102">Propriedade QueryDef.LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="66594-102">QueryDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="66594-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="66594-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="66594-104">Retorna a data e a hora da alteração mais recente feita em um objeto.</span><span class="sxs-lookup"><span data-stu-id="66594-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="66594-105">**Variant** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="66594-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="66594-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66594-106">Syntax</span></span>

<span data-ttu-id="66594-107">*expressão* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="66594-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="66594-108">*expressão* Uma variável que representa um objeto **QueryDef**.</span><span class="sxs-lookup"><span data-stu-id="66594-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="66594-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="66594-109">Remarks</span></span>

<span data-ttu-id="66594-p102">**DateCreated** e **LastUpdated** retornam a data e a hora nas quais o objeto foi criado ou atualizado pela última vez. Em um ambiente multiusuário, os usuários devem obter essas definições diretamente do servidor de arquivos para evitar discrepâncias nas definições das propriedades DateCreated e LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="66594-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

