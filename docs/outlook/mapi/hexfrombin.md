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
ms.openlocfilehash: 8f68de5e18d84c728241c188b932f99456f5be8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584832"
---
# <a name="hexfrombin"></a><span data-ttu-id="31173-103">HexFromBin</span><span class="sxs-lookup"><span data-stu-id="31173-103">HexFromBin</span></span>

  
  
<span data-ttu-id="31173-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31173-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31173-105">Converte um número binário em uma representação de cadeia de caracteres de um número hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="31173-105">Converts a binary number into a string representation of a hexadecimal number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="31173-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="31173-106">Header file:</span></span>  <br/> |<span data-ttu-id="31173-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="31173-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="31173-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="31173-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="31173-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="31173-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="31173-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="31173-110">Called by:</span></span>  <br/> |<span data-ttu-id="31173-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="31173-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a><span data-ttu-id="31173-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31173-112">Parameters</span></span>

 <span data-ttu-id="31173-113">_pb_</span><span class="sxs-lookup"><span data-stu-id="31173-113">_pb_</span></span>
  
> <span data-ttu-id="31173-114">[in] Ponteiro para os dados binários a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="31173-114">[in] Pointer to the binary data to be converted.</span></span> 
    
 <span data-ttu-id="31173-115">_cb_</span><span class="sxs-lookup"><span data-stu-id="31173-115">_cb_</span></span>
  
> <span data-ttu-id="31173-116">[in] Tamanho, em bytes, dos dados binários apontado pelo parâmetro _pb_ .</span><span class="sxs-lookup"><span data-stu-id="31173-116">[in] Size, in bytes, of the binary data pointed to by the  _pb_ parameter.</span></span> 
    
 <span data-ttu-id="31173-117">_SZ_</span><span class="sxs-lookup"><span data-stu-id="31173-117">_sz_</span></span>
  
> <span data-ttu-id="31173-118">[out] Ponteiro para uma cadeia de ASCII terminada em nulo, que representa os dados binários em dígitos hexadecimais.</span><span class="sxs-lookup"><span data-stu-id="31173-118">[out] Pointer to a null-terminated ASCII string representing the binary data in hexadecimal digits.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="31173-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="31173-119">Return value</span></span>

<span data-ttu-id="31173-120">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="31173-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="31173-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="31173-121">Remarks</span></span>

<span data-ttu-id="31173-122">A função **HexFromBin** usa um ponteiro para uma unidade de dados binários cujo tamanho é indicado pelo parâmetro _cb_ .</span><span class="sxs-lookup"><span data-stu-id="31173-122">The **HexFromBin** function takes a pointer to a unit of binary data whose size is indicated by the  _cb_ parameter.</span></span> <span data-ttu-id="31173-123">Ele retorna na cadeia de caracteres _sz_ contido em (2 \* _cb_) + 1 bytes de memória, uma representação dessas informações binárias em hexadecimais números.</span><span class="sxs-lookup"><span data-stu-id="31173-123">It returns in the  _sz_ string, within (2\*  _cb_)+1 bytes of memory, a representation of this binary information in hexadecimal numbers.</span></span> <span data-ttu-id="31173-124">Se o valor de byte é 10 decimal, por exemplo, a cadeia de caracteres hexadecimal será 0A, um byte caso se converte na cadeia de caracteres de dois bytes.</span><span class="sxs-lookup"><span data-stu-id="31173-124">If the byte value is decimal 10, for example, the hexadecimal string will be 0A, so one byte converts to two bytes in the string.</span></span> 
  

