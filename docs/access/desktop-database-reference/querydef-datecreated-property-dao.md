---
title: Propriedade QueryDef. DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: f7585b34-8314-fb9f-daa6-cd1a8ad59d91
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836910(v=office.15)
ms:contentKeyID: 48548763
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a4a120eed6c20db73e1c23f31ea9329d00da2f0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301068"
---
# <a name="querydefdatecreated-property-dao"></a><span data-ttu-id="3ca91-102">Propriedade QueryDef. DateCreated (DAO)</span><span class="sxs-lookup"><span data-stu-id="3ca91-102">QueryDef.DateCreated property (DAO)</span></span>


<span data-ttu-id="3ca91-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ca91-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3ca91-104">Retorna a hora e a data nas quais um objeto foi criado (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="3ca91-104">Returns the date and time that an object was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="3ca91-105">**Variant** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3ca91-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ca91-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3ca91-106">Syntax</span></span>

<span data-ttu-id="3ca91-107">*expressão* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="3ca91-107">*expression* .DateCreated</span></span>

<span data-ttu-id="3ca91-108">*expressão* Uma variável que representa um objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="3ca91-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ca91-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="3ca91-109">Remarks</span></span>

<span data-ttu-id="3ca91-p102">**DateCreated** e **LastUpdated** retornam a data e a hora nas quais o objeto foi criado ou atualizado pela última vez. Em um ambiente multiusuário, os usuários devem obter essas definições diretamente do servidor de arquivos para evitar discrepâncias nas definições das propriedades DateCreated e LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="3ca91-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

