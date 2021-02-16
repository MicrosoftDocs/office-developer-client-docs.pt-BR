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
description: 'Last modified: November 08, 2011'
ms.openlocfilehash: 6583765d4df7c7bfae9e7a62606beaa857874954
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408345"
---
# <a name="ipstoverride1setpersistedregistrations"></a><span data-ttu-id="d85b8-103">IPSTOVERRIDE1::SetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="d85b8-103">IPSTOVERRIDE1::SetPersistedRegistrations</span></span>

<span data-ttu-id="d85b8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d85b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d85b8-105">Registra arquivos de Pastas Particulares (.pst) para desbloqueio automático, evitando mais chamadas para o HrTrustedPSTOverrideHandlerCallback.</span><span class="sxs-lookup"><span data-stu-id="d85b8-105">Registers Personal Folders (.pst) files for automatic unlocking, avoiding further calls to the HrTrustedPSTOverrideHandlerCallback.</span></span>
  
```cpp
HRESULT SetPersistedRegistrations(
  SPropValue *pmval
);
```

## <a name="parameters"></a><span data-ttu-id="d85b8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d85b8-106">Parameters</span></span>

<span data-ttu-id="d85b8-107">_pmval_</span><span class="sxs-lookup"><span data-stu-id="d85b8-107">_pmval_</span></span>
  
> <span data-ttu-id="d85b8-108">[in] Uma [estrutura SPropValue](spropvalue.md) que contém um ponteiro para o caminho da biblioteca de vínculo dinâmico (DLL) a ser registrado.</span><span class="sxs-lookup"><span data-stu-id="d85b8-108">[in] An [SPropValue](spropvalue.md) structure that contains a pointer to the path of the dynamic-link library (DLL) to register.</span></span> <span data-ttu-id="d85b8-109">A estrutura tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="d85b8-109">The structure has the following characteristics:</span></span> 
    
   - <span data-ttu-id="d85b8-110">Uma ulPropTag de [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span><span class="sxs-lookup"><span data-stu-id="d85b8-110">A ulPropTag of [PROP_TAG](prop_tag.md)(PT_MV_UNICODE, PROP_ID_NULL).</span></span>
    
   - <span data-ttu-id="d85b8-111">Uma propriedade de valor MVszW definida como uma matriz de cadeias de caracteres Unicode terminadas por caractere nulo.</span><span class="sxs-lookup"><span data-stu-id="d85b8-111">An MVszW value property that is set to an array of null-terminated Unicode character strings.</span></span> <span data-ttu-id="d85b8-112">Para obter mais informações, [consulte o tópico SWStringArray.](swstringarray.md)</span><span class="sxs-lookup"><span data-stu-id="d85b8-112">For more information see the [SWStringArray](swstringarray.md) topic.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="d85b8-113">O SPropValue é armazenado em uma propriedade MAPI no intervalo interno do PST.</span><span class="sxs-lookup"><span data-stu-id="d85b8-113">The SPropValue is stored in a MAPI property in the PST's internal range.</span></span> <span data-ttu-id="d85b8-114">Essa propriedade está inacessível para aplicativos MAPI comuns.</span><span class="sxs-lookup"><span data-stu-id="d85b8-114">This property is inaccessible to ordinary MAPI applications.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="d85b8-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d85b8-115">Return value</span></span>

<span data-ttu-id="d85b8-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="d85b8-116">S_OK</span></span> 
  
> <span data-ttu-id="d85b8-117">A chamada de função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d85b8-117">The function call was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d85b8-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d85b8-118">Remarks</span></span>

<span data-ttu-id="d85b8-119">Registros persistentes podem afetar adversamente o desempenho de aplicativos, como o Outlook e o Windows Desktop Search, que abrem PSTs.</span><span class="sxs-lookup"><span data-stu-id="d85b8-119">Persisted registrations may adversely affect the performance of applications, such as Outlook and Windows Desktop Search, that open PSTs.</span></span> <span data-ttu-id="d85b8-120">Considere o efeito de desempenho ao usar ou expandir o uso de registros persistentes.</span><span class="sxs-lookup"><span data-stu-id="d85b8-120">Consider the performance effect when using or expanding the usage of persisted registrations.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d85b8-121">Esse método é implementado somente para Unicode.</span><span class="sxs-lookup"><span data-stu-id="d85b8-121">This method is implemented for Unicode only.</span></span> <span data-ttu-id="d85b8-122">Além disso, ele falhará preventivamente se qualquer um dos caminhos na matriz não tiver uma extensão de nome de arquivo .dll.</span><span class="sxs-lookup"><span data-stu-id="d85b8-122">Further, it will preemptively fail if any of the paths in the array do not have a file name extension of .dll.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d85b8-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="d85b8-123">See also</span></span>

- [<span data-ttu-id="d85b8-124">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d85b8-124">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md) 
- [<span data-ttu-id="d85b8-125">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d85b8-125">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

