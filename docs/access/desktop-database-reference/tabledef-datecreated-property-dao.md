---
title: Propriedade TableDef.DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2cf97df5d5861a3bb0fdac34ceabc8f732a87d5c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885595"
---
# <a name="tabledefdatecreated-property-dao"></a><span data-ttu-id="d5f7a-102">Propriedade TableDef.DateCreated (DAO)</span><span class="sxs-lookup"><span data-stu-id="d5f7a-102">TableDef.DateCreated Property (DAO)</span></span>


<span data-ttu-id="d5f7a-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="d5f7a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d5f7a-p101">Retorna a hora e a data nas quais um objeto foi criado (somente em espaços de trabalho do Microsoft Access). **Variant** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d5f7a-p101">Returns the date and time that an object was created (Microsoft Access workspaces only). Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5f7a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5f7a-106">Syntax</span></span>

<span data-ttu-id="d5f7a-107">*expressão* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="d5f7a-107">*expression* .DateCreated</span></span>

<span data-ttu-id="d5f7a-108">*expressão* Uma variável que representa um objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="d5f7a-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5f7a-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5f7a-109">Remarks</span></span>

<span data-ttu-id="d5f7a-p102">**DateCreated** e **LastUpdated** retornam a data e a hora em que o objeto foi criado ou atualizado pela última vez. Em um ambiente de vários usuários, os usuários devem obter essas configurações diretamente do servidor de arquivos para evitar discrepâncias nas configurações das propriedades DateCreated e LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="d5f7a-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

