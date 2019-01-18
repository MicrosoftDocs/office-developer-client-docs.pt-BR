---
title: Propriedade TableDef.DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5dc326b271e8444211bba0cd2d3c37c047ac205
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707021"
---
# <a name="tabledefdatecreated-property-dao"></a><span data-ttu-id="29788-102">Propriedade TableDef.DateCreated (DAO)</span><span class="sxs-lookup"><span data-stu-id="29788-102">TableDef.DateCreated property (DAO)</span></span>


<span data-ttu-id="29788-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="29788-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="29788-p101">Retorna a hora e a data nas quais um objeto foi criado (somente em espaços de trabalho do Microsoft Access). **Variant** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="29788-p101">Returns the date and time that an object was created (Microsoft Access workspaces only). Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="29788-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29788-106">Syntax</span></span>

<span data-ttu-id="29788-107">*expressão* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="29788-107">*expression* .DateCreated</span></span>

<span data-ttu-id="29788-108">*expressão* Uma variável que representa um objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="29788-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="29788-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="29788-109">Remarks</span></span>

<span data-ttu-id="29788-p102">**DateCreated** e **LastUpdated** retornam a data e a hora em que o objeto foi criado ou atualizado pela última vez. Em um ambiente de vários usuários, os usuários devem obter essas configurações diretamente do servidor de arquivos para evitar discrepâncias nas configurações das propriedades DateCreated e LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="29788-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

