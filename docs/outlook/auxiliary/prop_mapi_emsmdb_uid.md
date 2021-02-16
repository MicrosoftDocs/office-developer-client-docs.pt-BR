---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Representa uma estrutura ACCT_BIN que contém a UID de uma conta do Exchange.
ms.openlocfilehash: 6bb529da82cc24e41ddc70c5031f84050a2ece25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326548"
---
# <a name="prop_mapi_emsmdb_uid"></a><span data-ttu-id="a20fd-103">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="a20fd-103">PROP_MAPI_EMSMDB_UID</span></span>

<span data-ttu-id="a20fd-104">Representa uma estrutura [ACCT_BIN](acct_bin.md) que contém a UID de uma conta do Exchange.</span><span class="sxs-lookup"><span data-stu-id="a20fd-104">Represents an [ACCT_BIN](acct_bin.md) structure that contains the UID of an Exchange account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a20fd-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="a20fd-105">Quick info</span></span>

<span data-ttu-id="a20fd-106">Confira [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="a20fd-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a20fd-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a20fd-107">Identifier:</span></span>  <br/> |<span data-ttu-id="a20fd-108">0x2009</span><span class="sxs-lookup"><span data-stu-id="a20fd-108">0x2009</span></span>  <br/> |
|<span data-ttu-id="a20fd-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="a20fd-109">Property type:</span></span>  <br/> |<span data-ttu-id="a20fd-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="a20fd-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="a20fd-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="a20fd-111">Property tag:</span></span>  <br/> |<span data-ttu-id="a20fd-112">0x20090102</span><span class="sxs-lookup"><span data-stu-id="a20fd-112">0x20090102</span></span>  <br/> |
|<span data-ttu-id="a20fd-113">Acesso:</span><span class="sxs-lookup"><span data-stu-id="a20fd-113">Access:</span></span>  <br/> |<span data-ttu-id="a20fd-114">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a20fd-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a20fd-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a20fd-115">Remarks</span></span>

<span data-ttu-id="a20fd-116">Use essa propriedade por meio [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="a20fd-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="a20fd-117">Use [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) para verificar se a conta é uma conta do Exchange.</span><span class="sxs-lookup"><span data-stu-id="a20fd-117">Use [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) to verify if the account is an Exchange account.</span></span> <span data-ttu-id="a20fd-118">Se for, **PROP\_MAPI_EMSMDB_UID** será um **ACCT_BIN** que contém a **emsmdbUID**, que é a ID exclusiva da conta do Exchange.</span><span class="sxs-lookup"><span data-stu-id="a20fd-118">If it is, **PROP\_MAPI_EMSMDB_UID** is an **ACCT_BIN** that contains the **emsmdbUID**, which is the unique ID, for the Exchange account.</span></span> <span data-ttu-id="a20fd-119">Se a conta não for do Exchange, essa propriedade ficará indefinida.</span><span class="sxs-lookup"><span data-stu-id="a20fd-119">If the account is not an Exchange account, this property is undefined.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a20fd-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="a20fd-120">See also</span></span>

- [<span data-ttu-id="a20fd-121">Sobre a API de gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="a20fd-121">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="a20fd-122">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="a20fd-122">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="a20fd-123">Usar várias contas do Exchange</span><span class="sxs-lookup"><span data-stu-id="a20fd-123">Using Multiple Exchange Accounts</span></span>](https://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [<span data-ttu-id="a20fd-124">Propriedade canônica PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="a20fd-124">PidTagExchangeProfileSectionId Canonical Property</span></span>](https://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)

