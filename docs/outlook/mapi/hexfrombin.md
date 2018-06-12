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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: c1d333c7c019c30c3f6c6b3567453f2f022d4b5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766728"
---
# <a name="hexfrombin"></a><span data-ttu-id="61c76-103">HexFromBin</span><span class="sxs-lookup"><span data-stu-id="61c76-103">HexFromBin</span></span>

  
  
<span data-ttu-id="61c76-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="61c76-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="61c76-105">Converte um número binário em uma representação de cadeia de caracteres de um número hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="61c76-105">Converts a binary number into a string representation of a hexadecimal number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="61c76-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="61c76-106">Header file:</span></span>  <br/> |<span data-ttu-id="61c76-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="61c76-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="61c76-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="61c76-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="61c76-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="61c76-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="61c76-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="61c76-110">Called by:</span></span>  <br/> |<span data-ttu-id="61c76-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="61c76-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a><span data-ttu-id="61c76-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="61c76-112">Parameters</span></span>

 <span data-ttu-id="61c76-113">_pb_</span><span class="sxs-lookup"><span data-stu-id="61c76-113">_pb_</span></span>
  
> <span data-ttu-id="61c76-114">[in] Ponteiro para os dados binários a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="61c76-114">[in] Pointer to the binary data to be converted.</span></span> 
    
 <span data-ttu-id="61c76-115">_cb_</span><span class="sxs-lookup"><span data-stu-id="61c76-115">_cb_</span></span>
  
> <span data-ttu-id="61c76-116">[in] Tamanho, em bytes, dos dados binários apontado pelo parâmetro _pb_ .</span><span class="sxs-lookup"><span data-stu-id="61c76-116">[in] Size, in bytes, of the binary data pointed to by the  _pb_ parameter.</span></span> 
    
 <span data-ttu-id="61c76-117">_SZ_</span><span class="sxs-lookup"><span data-stu-id="61c76-117">_sz_</span></span>
  
> <span data-ttu-id="61c76-118">[out] Ponteiro para uma cadeia de ASCII terminada em nulo, que representa os dados binários em dígitos hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="61c76-118">[out] Pointer to a null-terminated ASCII string representing the binary data in hexadecimal digits.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="61c76-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="61c76-119">Return value</span></span>

<span data-ttu-id="61c76-120">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="61c76-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="61c76-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="61c76-121">Remarks</span></span>

<span data-ttu-id="61c76-122">A função **HexFromBin** usa um ponteiro para uma unidade de dados binários cujo tamanho é indicado pelo parâmetro _cb_ .</span><span class="sxs-lookup"><span data-stu-id="61c76-122">The **HexFromBin** function takes a pointer to a unit of binary data whose size is indicated by the  _cb_ parameter.</span></span> <span data-ttu-id="61c76-123">Ele retorna na cadeia de caracteres _sz_ contido em (2 \* _cb_) + 1 bytes de memória, uma representação dessas informações binárias em hexadecimais números.</span><span class="sxs-lookup"><span data-stu-id="61c76-123">It returns in the  _sz_ string, within (2\*  _cb_)+1 bytes of memory, a representation of this binary information in hexadecimal numbers.</span></span> <span data-ttu-id="61c76-124">Se o valor de byte é 10 decimal, por exemplo, a cadeia de caracteres hexadecimal será 0A, um byte caso se converte na cadeia de caracteres de dois bytes.</span><span class="sxs-lookup"><span data-stu-id="61c76-124">If the byte value is decimal 10, for example, the hexadecimal string will be 0A, so one byte converts to two bytes in the string.</span></span> 
  

