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
ms.openlocfilehash: d80c73aef780a0da39f3939f71462488a067de5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432944"
---
# <a name="removepreprocessinfo"></a><span data-ttu-id="f3a7b-103">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="f3a7b-103">RemovePreprocessInfo</span></span>

  
  
<span data-ttu-id="f3a7b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3a7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3a7b-105">Remove informações pré-processadas escritas por uma função baseada em [PreprocessMessage](preprocessmessage.md) de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-105">Removes preprocessed information written by a [PreprocessMessage](preprocessmessage.md) based function from a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f3a7b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f3a7b-106">Header file:</span></span>  <br/> |<span data-ttu-id="f3a7b-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="f3a7b-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="f3a7b-108">Função definida implementada por:</span><span class="sxs-lookup"><span data-stu-id="f3a7b-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="f3a7b-109">Provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="f3a7b-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="f3a7b-110">Função definida chamada por:</span><span class="sxs-lookup"><span data-stu-id="f3a7b-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="f3a7b-111">Spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="f3a7b-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a><span data-ttu-id="f3a7b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3a7b-112">Parameters</span></span>

 <span data-ttu-id="f3a7b-113">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="f3a7b-113">_lpMessage_</span></span>
  
> <span data-ttu-id="f3a7b-114">[in] Ponteiro para a mensagem pré-processada da qual as informações devem ser removidas.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-114">[in] Pointer to the preprocessed message from which information is to be removed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f3a7b-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f3a7b-115">Return value</span></span>

<span data-ttu-id="f3a7b-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3a7b-116">S_OK</span></span>
  
> <span data-ttu-id="f3a7b-117">As informações pré-processadas foram removidas com êxito.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-117">Preprocessed information was removed successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f3a7b-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3a7b-118">Remarks</span></span>

<span data-ttu-id="f3a7b-119">O spooler MAPI chama uma função com base **em RemovePreprocessInfo**.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-119">The MAPI spooler calls a function based on **RemovePreprocessInfo**.</span></span> <span data-ttu-id="f3a7b-120">Um provedor de transporte registra a função baseada **RemovePreprocessInfo** ao mesmo tempo em que registra a função baseada em **PreprocessMessage** paralela em uma chamada para o método [IMAPISupport::RegisterPreprocessor.](imapisupport-registerpreprocessor.md)</span><span class="sxs-lookup"><span data-stu-id="f3a7b-120">A transport provider registers the **RemovePreprocessInfo** based function at the same time it registers the parallel **PreprocessMessage** based function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> 
  
<span data-ttu-id="f3a7b-121">Uma renderização de imagem adequada para transmissão de fax é um exemplo de informações pré-processadas escritas por uma função definida pelo protótipo de função [PreprocessMessage.](preprocessmessage.md)</span><span class="sxs-lookup"><span data-stu-id="f3a7b-121">An image rendering suitable for fax transmission is an example of preprocessed information written by a function defined by the [PreprocessMessage](preprocessmessage.md)function prototype.</span></span> <span data-ttu-id="f3a7b-122">O spooler MAPI geralmente chama uma **função RemovePreprocessInfo** depois de enviar uma mensagem que contém informações pré-processadas.</span><span class="sxs-lookup"><span data-stu-id="f3a7b-122">The MAPI spooler usually calls a **RemovePreprocessInfo** function after sending a message that contains preprocessed information.</span></span> 
  

