---
title: Propriedade TableDef. DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5dc326b271e8444211bba0cd2d3c37c047ac205
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314536"
---
# <a name="tabledefdatecreated-property-dao"></a><span data-ttu-id="2d49f-102">Propriedade TableDef. DateCreated (DAO)</span><span class="sxs-lookup"><span data-stu-id="2d49f-102">TableDef.DateCreated property (DAO)</span></span>


<span data-ttu-id="2d49f-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d49f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d49f-104">Retorna a hora e a data nas quais um objeto foi criado (somente em espaços de trabalho do Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="2d49f-104">Returns the date and time that an object was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="2d49f-105">**Variant** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="2d49f-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d49f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d49f-106">Syntax</span></span>

<span data-ttu-id="2d49f-107">*expressão* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="2d49f-107">*expression* .DateCreated</span></span>

<span data-ttu-id="2d49f-108">*expressão* Uma variável que representa um objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="2d49f-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d49f-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d49f-109">Remarks</span></span>

<span data-ttu-id="2d49f-p102">**DateCreated** e **LastUpdated** retornam a data e a hora nas quais o objeto foi criado ou atualizado pela última vez. Em um ambiente multiusuário, os usuários devem obter essas definições diretamente do servidor de arquivos para evitar discrepâncias nas definições das propriedades DateCreated e LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="2d49f-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

