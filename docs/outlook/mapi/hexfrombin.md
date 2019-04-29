---
title: HexFromBin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HexFromBin
api_type:
- COM
ms.assetid: 12b95657-1926-4a24-be63-40305ea6f990
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a1bf02de914865e27c8c018aba8695c858888ae2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412573"
---
# <a name="hexfrombin"></a><span data-ttu-id="29dfb-103">HexFromBin</span><span class="sxs-lookup"><span data-stu-id="29dfb-103">HexFromBin</span></span>

  
  
<span data-ttu-id="29dfb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29dfb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29dfb-105">Converte um número binário em uma representação de cadeia de caracteres de um número hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="29dfb-105">Converts a binary number into a string representation of a hexadecimal number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29dfb-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="29dfb-106">Header file:</span></span>  <br/> |<span data-ttu-id="29dfb-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="29dfb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="29dfb-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="29dfb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="29dfb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="29dfb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="29dfb-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="29dfb-110">Called by:</span></span>  <br/> |<span data-ttu-id="29dfb-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="29dfb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a><span data-ttu-id="29dfb-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29dfb-112">Parameters</span></span>

 <span data-ttu-id="29dfb-113">_pb_</span><span class="sxs-lookup"><span data-stu-id="29dfb-113">_pb_</span></span>
  
> <span data-ttu-id="29dfb-114">no Ponteiro para os dados binários a serem convertidos.</span><span class="sxs-lookup"><span data-stu-id="29dfb-114">[in] Pointer to the binary data to be converted.</span></span> 
    
 <span data-ttu-id="29dfb-115">_cb_</span><span class="sxs-lookup"><span data-stu-id="29dfb-115">_cb_</span></span>
  
> <span data-ttu-id="29dfb-116">no Tamanho, em bytes, dos dados binários apontados pelo parâmetro _PB_ .</span><span class="sxs-lookup"><span data-stu-id="29dfb-116">[in] Size, in bytes, of the binary data pointed to by the  _pb_ parameter.</span></span> 
    
 <span data-ttu-id="29dfb-117">_v_</span><span class="sxs-lookup"><span data-stu-id="29dfb-117">_sz_</span></span>
  
> <span data-ttu-id="29dfb-118">bota Ponteiro para uma cadeia de caracteres ASCII terminada em nulo que representa os dados binários em dígitos hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="29dfb-118">[out] Pointer to a null-terminated ASCII string representing the binary data in hexadecimal digits.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="29dfb-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="29dfb-119">Return value</span></span>

<span data-ttu-id="29dfb-120">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="29dfb-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="29dfb-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="29dfb-121">Remarks</span></span>

<span data-ttu-id="29dfb-122">A função **HexFromBin** usa um ponteiro para uma unidade de dados binários cujo tamanho é indicado pelo parâmetro _CB_ .</span><span class="sxs-lookup"><span data-stu-id="29dfb-122">The **HexFromBin** function takes a pointer to a unit of binary data whose size is indicated by the  _cb_ parameter.</span></span> <span data-ttu-id="29dfb-123">Ele retorna na cadeia de caracteres _sz_ , dentro (2 \* _CB_) + 1 bytes de memória, uma representação dessas informações binárias em números hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="29dfb-123">It returns in the  _sz_ string, within (2\*  _cb_)+1 bytes of memory, a representation of this binary information in hexadecimal numbers.</span></span> <span data-ttu-id="29dfb-124">Se o valor de byte for Decimal 10, por exemplo, a cadeia de caracteres hexadecimal será 0A, então um byte é convertido em dois bytes na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="29dfb-124">If the byte value is decimal 10, for example, the hexadecimal string will be 0A, so one byte converts to two bytes in the string.</span></span> 
  

