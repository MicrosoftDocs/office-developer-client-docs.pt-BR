---
title: RemovePreprocessInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.RemovePreprocessInfo
api_type:
- COM
ms.assetid: 25f46937-abac-4a0b-83db-eeac9451c112
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fab8860621cee5a87b087ee9d98f373baa278e45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770264"
---
# <a name="removepreprocessinfo"></a><span data-ttu-id="fccc6-103">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="fccc6-103">RemovePreprocessInfo</span></span>

  
  
<span data-ttu-id="fccc6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fccc6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fccc6-105">Remove preprocessada informações escritas por uma função [PreprocessMessage](preprocessmessage.md) com base em uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="fccc6-105">Removes preprocessed information written by a [PreprocessMessage](preprocessmessage.md) based function from a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fccc6-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="fccc6-106">Header file:</span></span>  <br/> |<span data-ttu-id="fccc6-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="fccc6-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="fccc6-108">Função definido implementada por:</span><span class="sxs-lookup"><span data-stu-id="fccc6-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="fccc6-109">Provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="fccc6-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="fccc6-110">Função definido chamada pelo:</span><span class="sxs-lookup"><span data-stu-id="fccc6-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="fccc6-111">Spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="fccc6-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="fccc6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fccc6-112">Parameters</span></span>

 <span data-ttu-id="fccc6-113">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="fccc6-113">_lpMessage_</span></span>
  
> <span data-ttu-id="fccc6-114">[in] Ponteiro para a mensagem pré-processado do qual as informações são a ser removido.</span><span class="sxs-lookup"><span data-stu-id="fccc6-114">[in] Pointer to the preprocessed message from which information is to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fccc6-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="fccc6-115">Return value</span></span>

<span data-ttu-id="fccc6-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="fccc6-116">S_OK</span></span>
  
> <span data-ttu-id="fccc6-117">Informações pré-processado foi removidas com êxito.</span><span class="sxs-lookup"><span data-stu-id="fccc6-117">Preprocessed information was removed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fccc6-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="fccc6-118">Remarks</span></span>

<span data-ttu-id="fccc6-119">O MAPI spooler chama uma função com base em **RemovePreprocessInfo**.</span><span class="sxs-lookup"><span data-stu-id="fccc6-119">The MAPI spooler calls a function based on **RemovePreprocessInfo**.</span></span> <span data-ttu-id="fccc6-120">Um provedor de transporte registra a função **RemovePreprocessInfo** com base ao mesmo tempo em que ele registra a função de **PreprocessMessage** com base em paralelo em uma chamada ao método [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="fccc6-120">A transport provider registers the **RemovePreprocessInfo** based function at the same time it registers the parallel **PreprocessMessage** based function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> 
  
<span data-ttu-id="fccc6-121">Uma imagem de renderização adequado para a transmissão de fax é um exemplo de informação pré-processado escrito por uma função definida pelo protótipo de função [PreprocessMessage](preprocessmessage.md).</span><span class="sxs-lookup"><span data-stu-id="fccc6-121">An image rendering suitable for fax transmission is an example of preprocessed information written by a function defined by the [PreprocessMessage](preprocessmessage.md)function prototype.</span></span> <span data-ttu-id="fccc6-122">O MAPI spooler geralmente chama uma função de **RemovePreprocessInfo** após enviar uma mensagem que contém informações pré-processado.</span><span class="sxs-lookup"><span data-stu-id="fccc6-122">The MAPI spooler usually calls a **RemovePreprocessInfo** function after sending a message that contains preprocessed information.</span></span> 
  
