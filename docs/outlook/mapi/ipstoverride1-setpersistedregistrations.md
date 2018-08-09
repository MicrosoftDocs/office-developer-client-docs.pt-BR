---
title: IPSTOVERRIDE1SetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.SetPersistedRegistrations
api_type:
- COM
ms.assetid: 5f4b62db-a759-41a2-9bea-29fc04b2962b
description: 'Modificado pela última vez: 08 de novembro de 2011'
ms.openlocfilehash: 9895c558af94eebebe2dacdb6f9bf674e3de6263
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767679"
---
# <a name="ipstoverride1setpersistedregistrations"></a><span data-ttu-id="8e5a2-103">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="8e5a2-103">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>

<span data-ttu-id="8e5a2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e5a2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8e5a2-105">Registra os arquivos de pastas particulares (. pst) para desbloqueio automático, evitando mais chamadas para o HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="8e5a2-105">Registers Personal Folders (.pst) files for automatic unlocking, avoiding further calls to the HrTrustedPSTOverrideHandlerCallback.</span></span>
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a><span data-ttu-id="8e5a2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e5a2-106">Parameters</span></span>

<span data-ttu-id="8e5a2-107">_pmval_</span><span class="sxs-lookup"><span data-stu-id="8e5a2-107">_pmval_</span></span>
  
> <span data-ttu-id="8e5a2-108">[in] Uma estrutura de [SPropValue](spropvalue.md) que contém um ponteiro para o caminho da biblioteca de vínculo dinâmico (DLL) para registrar.</span><span class="sxs-lookup"><span data-stu-id="8e5a2-108">[in] An [SPropValue](spropvalue.md) structure that contains a pointer to the path of the dynamic-link library (DLL) to register.</span></span> <span data-ttu-id="8e5a2-109">A estrutura tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="8e5a2-109">The structure has the following characteristics:</span></span> 
    
   - <span data-ttu-id="8e5a2-110">Um ulPropTag de [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="8e5a2-110">A ulPropTag of [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span></span>
    
   - <span data-ttu-id="8e5a2-111">Uma propriedade de valor de MVszW é definida como uma matriz de cadeias de caracteres Unicode terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="8e5a2-111">An MVszW value property that is set to an array of null-terminated Unicode character strings.</span></span> <span data-ttu-id="8e5a2-112">Para obter mais informações, consulte o tópico de [SWStringArray](swstringarray.md) .</span><span class="sxs-lookup"><span data-stu-id="8e5a2-112">For more information see the [SWStringArray](swstringarray.md) topic.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="8e5a2-113">O SPropValue é armazenado em uma propriedade MAPI no intervalo de interno do PST.</span><span class="sxs-lookup"><span data-stu-id="8e5a2-113">The SPropValue is stored in a MAPI property in the PST's internal range.</span></span> <span data-ttu-id="8e5a2-114">Essa propriedade está inacessível aos aplicativos comuns de MAPI.</span><span class="sxs-lookup"><span data-stu-id="8e5a2-114">This property is inaccessible to ordinary MAPI applications.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="8e5a2-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8e5a2-115">Return value</span></span>

<span data-ttu-id="8e5a2-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="8e5a2-116">S_OK</span></span> 
  
> <span data-ttu-id="8e5a2-117">A chamada de função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8e5a2-117">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8e5a2-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e5a2-118">Remarks</span></span>

<span data-ttu-id="8e5a2-119">Os registros persistentes podem afetar negativamente o desempenho de aplicativos, como o Outlook e Windows Desktop Search, que PSTs ser aberto.</span><span class="sxs-lookup"><span data-stu-id="8e5a2-119">Persisted registrations may adversely affect the performance of applications, such as Outlook and Windows Desktop Search, that open PSTs.</span></span> <span data-ttu-id="8e5a2-120">Considere o efeito no desempenho ao usar ou expandindo o uso dos registros persistentes.</span><span class="sxs-lookup"><span data-stu-id="8e5a2-120">Consider the performance effect when using or expanding the usage of persisted registrations.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="8e5a2-121">Esse método é implementado apenas para Unicode.</span><span class="sxs-lookup"><span data-stu-id="8e5a2-121">This method is implemented for Unicode only.</span></span> <span data-ttu-id="8e5a2-122">Além disso, ele preventivamente falhará se qualquer um dos caminhos na matriz não têm uma extensão de nome de arquivo de. dll.</span><span class="sxs-lookup"><span data-stu-id="8e5a2-122">Further, it will preemptively fail if any of the paths in the array do not have a file name extension of .dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8e5a2-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e5a2-123">See also</span></span>

- [<span data-ttu-id="8e5a2-124">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e5a2-124">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md) 
- [<span data-ttu-id="8e5a2-125">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e5a2-125">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

