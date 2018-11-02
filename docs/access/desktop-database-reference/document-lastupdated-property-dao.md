---
title: Propriedade Document.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 57fb558330c602206831c1c72f09a13094eba799
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927309"
---
# <a name="documentlastupdated-property-dao"></a><span data-ttu-id="efe9f-102">Propriedade Document.LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="efe9f-102">Document.LastUpdated property (DAO)</span></span>


<span data-ttu-id="efe9f-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="efe9f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="efe9f-p101">Retorna a data e a hora da alteração feita mais recentemente em um objeto. **Variant** somente leitura.</span><span class="sxs-lookup"><span data-stu-id="efe9f-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="efe9f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="efe9f-106">Syntax</span></span>

<span data-ttu-id="efe9f-107">*expressão* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="efe9f-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="efe9f-108">*expressão* Uma variável que representa um objeto **Document** .</span><span class="sxs-lookup"><span data-stu-id="efe9f-108">*expression* A variable that represents a **Document** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="efe9f-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="efe9f-109">Remarks</span></span>

<span data-ttu-id="efe9f-p102">**DateCreated** e **LastUpdated** retornam a data e a hora em que o objeto foi criado ou atualizado pela última vez. Em um ambiente de vários usuários, os usuários devem obter essas configurações diretamente do servidor de arquivos para evitar discrepâncias nas configurações das propriedades DateCreated e LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="efe9f-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

