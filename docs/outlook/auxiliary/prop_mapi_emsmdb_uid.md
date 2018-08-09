---
title: PROP_MAPI_EMSMDB_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8e5b42e3-844f-488c-ba6f-b74c447b1d59
description: Representa uma estrutura ACCT_BIN que contém o UID de uma conta do Exchange.
ms.openlocfilehash: 05e2e61601a08e0cb6f6dc99d265f12a10b19d3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766080"
---
# <a name="propmapiemsmdbuid"></a><span data-ttu-id="d0231-103">PROP_MAPI_EMSMDB_UID</span><span class="sxs-lookup"><span data-stu-id="d0231-103">PROP_MAPI_EMSMDB_UID</span></span>

<span data-ttu-id="d0231-104">Representa uma estrutura [ACCT_BIN](acct_bin.md) que contém o UID de uma conta do Exchange.</span><span class="sxs-lookup"><span data-stu-id="d0231-104">Represents an [ACCT_BIN](acct_bin.md) structure that contains the UID of an Exchange account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="d0231-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="d0231-105">Quick info</span></span>

<span data-ttu-id="d0231-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="d0231-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d0231-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d0231-107">Identifier:</span></span>  <br/> |<span data-ttu-id="d0231-108">0x2009</span><span class="sxs-lookup"><span data-stu-id="d0231-108">0x2009</span></span>  <br/> |
|<span data-ttu-id="d0231-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="d0231-109">Property type:</span></span>  <br/> |<span data-ttu-id="d0231-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d0231-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d0231-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="d0231-111">Property tag:</span></span>  <br/> |<span data-ttu-id="d0231-112">0x20090102</span><span class="sxs-lookup"><span data-stu-id="d0231-112">0x20090102</span></span>  <br/> |
|<span data-ttu-id="d0231-113">Access:</span><span class="sxs-lookup"><span data-stu-id="d0231-113">Access:</span></span>  <br/> |<span data-ttu-id="d0231-114">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d0231-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0231-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0231-115">Remarks</span></span>

<span data-ttu-id="d0231-116">Obtenha essa propriedade usando [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="d0231-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="d0231-117">Use [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) para verificar se a conta é uma conta do Exchange.</span><span class="sxs-lookup"><span data-stu-id="d0231-117">Use [PROP_ACCT_IS_EXCH](prop_acct_is_exch.md) to verify if the account is an Exchange account.</span></span> <span data-ttu-id="d0231-118">Se estiver, **PROP\_MAPI_EMSMDB_UID** é um **ACCT_BIN** que contém o **emsmdbUID**, que é a ID exclusiva, para a conta do Exchange.</span><span class="sxs-lookup"><span data-stu-id="d0231-118">If it is, **PROP\_MAPI_EMSMDB_UID** is an **ACCT_BIN** that contains the **emsmdbUID**, which is the unique ID, for the Exchange account.</span></span> <span data-ttu-id="d0231-119">Se a conta não for uma conta do Exchange, essa propriedade é indefinida.</span><span class="sxs-lookup"><span data-stu-id="d0231-119">If the account is not an Exchange account, this property is undefined.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d0231-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0231-120">See also</span></span>

- [<span data-ttu-id="d0231-121">Sobre a API de gerenciamento de conta</span><span class="sxs-lookup"><span data-stu-id="d0231-121">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="d0231-122">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="d0231-122">Constants (Account management API)</span></span>](constants-account-management-api.md)
- [<span data-ttu-id="d0231-123">Usar várias contas do Exchange</span><span class="sxs-lookup"><span data-stu-id="d0231-123">Using Multiple Exchange Accounts</span></span>](http://msdn.microsoft.com/library/4e1804bf-4c50-4942-a7ab-9a8caf1be7e5%28Office.15%29.aspx)  
- [<span data-ttu-id="d0231-124">Propriedade canônica PidTagExchangeProfileSectionId</span><span class="sxs-lookup"><span data-stu-id="d0231-124">PidTagExchangeProfileSectionId Canonical Property</span></span>](http://msdn.microsoft.com/library/4ad2f417-be8f-4fc8-9321-82097289074b%28Office.15%29.aspx)

