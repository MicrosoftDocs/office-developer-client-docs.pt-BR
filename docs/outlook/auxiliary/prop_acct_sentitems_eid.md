---
title: PROP_ACCT_SENTITEMS_EID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f199a97f-55d6-9297-adc4-e9f7b4b5f58b
description: Representa a ID de entrada da pasta padrão para itens enviados da conta.
ms.openlocfilehash: 24bb4714a4f4964ac3d84ea7a792e64da67599df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431838"
---
# <a name="prop_acct_sentitems_eid"></a><span data-ttu-id="877b4-103">PROP_ACCT_SENTITEMS_EID</span><span class="sxs-lookup"><span data-stu-id="877b4-103">PROP_ACCT_SENTITEMS_EID</span></span>

<span data-ttu-id="877b4-104">Representa a ID de entrada da pasta padrão para itens enviados da conta.</span><span class="sxs-lookup"><span data-stu-id="877b4-104">Represents the Entry ID of the default folder for sent items for the account.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="877b4-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="877b4-105">Quick info</span></span>

<span data-ttu-id="877b4-106">Confira [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="877b4-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="877b4-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="877b4-107">Identifier:</span></span>  <br/> |<span data-ttu-id="877b4-108">0x0020</span><span class="sxs-lookup"><span data-stu-id="877b4-108">0x0020</span></span>  <br/> |
|<span data-ttu-id="877b4-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="877b4-109">Property type:</span></span>  <br/> |<span data-ttu-id="877b4-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="877b4-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="877b4-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="877b4-111">Property tag:</span></span>  <br/> |<span data-ttu-id="877b4-112">0x00200102</span><span class="sxs-lookup"><span data-stu-id="877b4-112">0x00200102</span></span>  <br/> |
|<span data-ttu-id="877b4-113">Acesso:</span><span class="sxs-lookup"><span data-stu-id="877b4-113">Access:</span></span>  <br/> |<span data-ttu-id="877b4-114">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="877b4-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="877b4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="877b4-115">Remarks</span></span>

<span data-ttu-id="877b4-116">Use essa propriedade por meio [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="877b4-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span>
  
<span data-ttu-id="877b4-117">A pasta padrão para itens enviados é **Itens Enviados.**</span><span class="sxs-lookup"><span data-stu-id="877b4-117">The default folder for sent items is **Sent Items**.</span></span>
  
<span data-ttu-id="877b4-118">Essa propriedade é somente leitura para contas POP3 e IMAP.</span><span class="sxs-lookup"><span data-stu-id="877b4-118">This property is read-only for POP3 and IMAP accounts.</span></span> <span data-ttu-id="877b4-119">Tentar definir essa propriedade para esses tipos de contas **retorna** E_ACCT_NOT_FOUND .</span><span class="sxs-lookup"><span data-stu-id="877b4-119">Attempting to set this property for these types of accounts returns **E_ACCT_NOT_FOUND**.</span></span> 
  

