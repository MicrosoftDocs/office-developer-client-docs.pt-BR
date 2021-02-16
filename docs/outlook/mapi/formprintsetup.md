---
title: FORMPRINTSETUP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FORMPRINTSETUP
api_type:
- COM
ms.assetid: 6e82fe94-47bd-4a25-b25b-0ab6fe2db274
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c2b9176e21341ef28e6f0bc007757b097a05daee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327283"
---
# <a name="formprintsetup"></a><span data-ttu-id="47293-103">FORMPRINTSETUP</span><span class="sxs-lookup"><span data-stu-id="47293-103">FORMPRINTSETUP</span></span>

  
  
<span data-ttu-id="47293-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47293-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47293-105">Descreve as informações de configuração de impressão para o objeto de formulário.</span><span class="sxs-lookup"><span data-stu-id="47293-105">Describes the print setup information for the form object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="47293-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="47293-106">Header file:</span></span>  <br/> |<span data-ttu-id="47293-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="47293-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG ulFlags;
  HDEVMODE hDevMode;
  HDEVNAMES hDevNames;
  ULONG ulFirstPageNumber;
  ULONG ulFPrintAttachments;
} FORMPRINTSETUP, FAR * LPFORMPRINTSETUP;

```

## <a name="members"></a><span data-ttu-id="47293-108">Membros</span><span class="sxs-lookup"><span data-stu-id="47293-108">Members</span></span>

 <span data-ttu-id="47293-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="47293-109">**ulFlags**</span></span>
  
> <span data-ttu-id="47293-110">Máscara de bits de sinalizadores que controla o tipo das cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="47293-110">Bitmask of flags that controls the type of the strings.</span></span> <span data-ttu-id="47293-111">O sinalizador a seguir pode ser usado:</span><span class="sxs-lookup"><span data-stu-id="47293-111">The following flag can be used:</span></span>
    
<span data-ttu-id="47293-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="47293-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="47293-113">As cadeias de caracteres estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="47293-113">The strings are in Unicode format.</span></span> <span data-ttu-id="47293-114">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="47293-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="47293-115">**hDevmode**</span><span class="sxs-lookup"><span data-stu-id="47293-115">**hDevmode**</span></span>
  
> <span data-ttu-id="47293-116">Alça para o modo da impressora.</span><span class="sxs-lookup"><span data-stu-id="47293-116">Handle to the mode of the printer.</span></span>
    
 <span data-ttu-id="47293-117">**hDevnames**</span><span class="sxs-lookup"><span data-stu-id="47293-117">**hDevnames**</span></span>
  
> <span data-ttu-id="47293-118">Alça para o caminho da impressora.</span><span class="sxs-lookup"><span data-stu-id="47293-118">Handle to the path of the printer.</span></span>
    
 <span data-ttu-id="47293-119">**ulFirstPageNumber**</span><span class="sxs-lookup"><span data-stu-id="47293-119">**ulFirstPageNumber**</span></span>
  
> <span data-ttu-id="47293-120">Número de página da primeira página a ser impressa.</span><span class="sxs-lookup"><span data-stu-id="47293-120">Page number of the first page to be printed.</span></span>
    
 <span data-ttu-id="47293-121">**ulFPrintAttachments**</span><span class="sxs-lookup"><span data-stu-id="47293-121">**ulFPrintAttachments**</span></span>
  
> <span data-ttu-id="47293-122">Sinalizador que indica se há anexos a serem impressos.</span><span class="sxs-lookup"><span data-stu-id="47293-122">Flag that indicates whether there are attachments to be printed.</span></span> <span data-ttu-id="47293-123">Se houver anexos para imprimir, o **membro ulFPrintAttachments** será definido como 1.</span><span class="sxs-lookup"><span data-stu-id="47293-123">If there are attachments to print, the **ulFPrintAttachments** member is set to 1.</span></span> <span data-ttu-id="47293-124">Se não houver anexos para imprimir, ele será definido como 0.</span><span class="sxs-lookup"><span data-stu-id="47293-124">If there are no attachments to print, it is set to 0.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="47293-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="47293-125">Remarks</span></span>

<span data-ttu-id="47293-126">A **estrutura FORMPRINTSETUP** é usada para descrever as informações de configuração de impressão de um objeto de formulário.</span><span class="sxs-lookup"><span data-stu-id="47293-126">The **FORMPRINTSETUP** structure is used to describe the print setup information for a form object.</span></span> <span data-ttu-id="47293-127">Implementações de [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) preenchem a estrutura **FORMPRINTSETUP** e o retornam no conteúdo do parâmetro de saída  _lppFormPrintSetup_ de **GetPrintSetup**.</span><span class="sxs-lookup"><span data-stu-id="47293-127">Implementations of [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) fill in the **FORMPRINTSETUP** structure and return it in the contents of the  _lppFormPrintSetup_ output parameter of **GetPrintSetup**.</span></span>
  
<span data-ttu-id="47293-128">Se o sinalizador MAPI_UNICODE for passado no parâmetro  _ulFlags_ de **GetPrintSetup**, as cadeias de caracteres referenciadas pelos membros **hDevmode** e **hDevnames** deverão estar no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="47293-128">If the MAPI_UNICODE flag is passed in the  _ulFlags_ parameter of **GetPrintSetup**, the strings referenced by the **hDevmode** and **hDevnames** members should be in Unicode format.</span></span> <span data-ttu-id="47293-129">Caso contrário, as cadeias de caracteres devem estar no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="47293-129">Otherwise, the strings should be in ANSI format.</span></span> 
  
<span data-ttu-id="47293-130">Visualizadores de formulário implementando **IMAPIViewContext** devem alocar a estrutura **FORMPRINTSETUP** usando a função de alocador [MAPIAllocateBuffer](mapiallocatebuffer.md), mas alocar os membros individuais, **hDevMode** e **hDevNames**, com a função [Windows GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110).</span><span class="sxs-lookup"><span data-stu-id="47293-130">Form viewers implementing **IMAPIViewContext** must allocate the **FORMPRINTSETUP** structure using the MAPI allocator function [MAPIAllocateBuffer](mapiallocatebuffer.md), but allocate the individual members, **hDevMode** and **hDevNames**, with the Windows function [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110).</span></span> <span data-ttu-id="47293-131">A liberação de memória é tratada da mesma forma.</span><span class="sxs-lookup"><span data-stu-id="47293-131">The release of memory is handled similarly.</span></span> <span data-ttu-id="47293-132">Os **membros hDevMode** e **hDevNames** devem ser liberados usando a função [Windows GlobalFree,](https://go.microsoft.com/fwlink/?LinkId=132108) enquanto a estrutura **FORMPRINTSETUP** deve ser liberada com a função [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="47293-132">The **hDevMode** and **hDevNames** members must be freed using the Windows function [GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108) whereas the **FORMPRINTSETUP** structure must be freed with the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="47293-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="47293-133">See also</span></span>



[<span data-ttu-id="47293-134">IMAPIViewContext::GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="47293-134">IMAPIViewContext::GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md)
  
[<span data-ttu-id="47293-135">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="47293-135">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="47293-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="47293-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)


[<span data-ttu-id="47293-137">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="47293-137">MAPI Structures</span></span>](mapi-structures.md)

