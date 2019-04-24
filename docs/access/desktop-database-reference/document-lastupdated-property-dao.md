---
title: Propriedade Document. LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: abb766f7a47cbacaededf65eb2b5e9145bf88c60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293802"
---
# <a name="documentlastupdated-property-dao"></a><span data-ttu-id="5b040-102">Propriedade Document. LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="5b040-102">Document.LastUpdated property (DAO)</span></span>


<span data-ttu-id="5b040-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5b040-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5b040-104">Retorna a data e a hora da alteração mais recente feita em um objeto.</span><span class="sxs-lookup"><span data-stu-id="5b040-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="5b040-105">**Variant** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="5b040-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b040-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b040-106">Syntax</span></span>

<span data-ttu-id="5b040-107">*expressão* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="5b040-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="5b040-108">*expressão* Uma variável que representa um objeto **Document** .</span><span class="sxs-lookup"><span data-stu-id="5b040-108">*expression* A variable that represents a **Document** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b040-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b040-109">Remarks</span></span>

<span data-ttu-id="5b040-p102">**DateCreated** e **LastUpdated** retornam a data e a hora nas quais o objeto foi criado ou atualizado pela última vez. Em um ambiente multiusuário, os usuários devem obter essas definições diretamente do servidor de arquivos para evitar discrepâncias nas definições das propriedades DateCreated e LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="5b040-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

