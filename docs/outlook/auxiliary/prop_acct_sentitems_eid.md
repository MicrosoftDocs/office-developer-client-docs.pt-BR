---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Representa a identificação de entrada da pasta padrão para itens enviados para a conta.
ms.openlocfilehash: 7795e8a112f0575b764fd55e92d27c7085e3d3a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766051"
---
# <a name="propacctsentitemseid"></a><span data-ttu-id="3b2e7-103">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="3b2e7-103">PROP_ACCT_SENTITEMS_EID</span></span>

<span data-ttu-id="3b2e7-104">Representa a identificação de entrada da pasta padrão para itens enviados para a conta.</span><span class="sxs-lookup"><span data-stu-id="3b2e7-104">Represents the Entry ID of the default folder for sent items for the account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="3b2e7-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="3b2e7-105">Quick info</span></span>

<span data-ttu-id="3b2e7-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="3b2e7-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3b2e7-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3b2e7-107">Identifier:</span></span>  <br/> |<span data-ttu-id="3b2e7-108">0x0020</span><span class="sxs-lookup"><span data-stu-id="3b2e7-108">0x0020</span></span>  <br/> |
|<span data-ttu-id="3b2e7-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="3b2e7-109">Property type:</span></span>  <br/> |<span data-ttu-id="3b2e7-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3b2e7-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3b2e7-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="3b2e7-111">Property tag:</span></span>  <br/> |<span data-ttu-id="3b2e7-112">0x00200102</span><span class="sxs-lookup"><span data-stu-id="3b2e7-112">0x00200102</span></span>  <br/> |
|<span data-ttu-id="3b2e7-113">Access:</span><span class="sxs-lookup"><span data-stu-id="3b2e7-113">Access:</span></span>  <br/> |<span data-ttu-id="3b2e7-114">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3b2e7-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b2e7-115">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="3b2e7-115">Remarks</span></span>

<span data-ttu-id="3b2e7-116">Obtenha essa propriedade usando [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="3b2e7-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="3b2e7-117">A pasta padrão para itens enviados é **Itens enviados**.</span><span class="sxs-lookup"><span data-stu-id="3b2e7-117">The default folder for sent items is **Sent Items**.</span></span>
  
<span data-ttu-id="3b2e7-118">Essa propriedade é somente leitura para contas POP3 e IMAP.</span><span class="sxs-lookup"><span data-stu-id="3b2e7-118">This property is read-only for POP3 and IMAP accounts.</span></span> <span data-ttu-id="3b2e7-119">Tentar definir essa propriedade para esses tipos de contas retorna **E_ACCT_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="3b2e7-119">Attempting to set this property for these types of accounts returns **E_ACCT_NOT_FOUND**.</span></span> 
  

