---
title: Tratamento de erros no MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d98b7cf1d6c5cdc8517ea2e653115d9a7c01e3c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593295"
---
# <a name="error-handling-in-mapi"></a><span data-ttu-id="a028a-103">Tratamento de erros no MAPI</span><span class="sxs-lookup"><span data-stu-id="a028a-103">Error handling in MAPI</span></span>

<span data-ttu-id="a028a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a028a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a028a-105">Os valores de sucesso, aviso e erro são retornados usando um número de 32 bits, conhecido como resultado alça ou HRESULT.</span><span class="sxs-lookup"><span data-stu-id="a028a-105">Success, warning, and error values are returned using a 32-bit number known as a result handle, or HRESULT.</span></span> <span data-ttu-id="a028a-106">Um HRESULT não é realmente uma alça nada; ele é meramente um valor de 32 bits com vários campos codificados em que o valor.</span><span class="sxs-lookup"><span data-stu-id="a028a-106">An HRESULT is really not a handle to anything; it is merely a 32-bit value with several fields encoded in the value.</span></span> <span data-ttu-id="a028a-107">Um resultado de zero indica êxito e um resultado diferente de zero indica uma falha.</span><span class="sxs-lookup"><span data-stu-id="a028a-107">A zero result indicates success and a nonzero result indicates failure.</span></span>
  
<span data-ttu-id="a028a-108">MAPI em plataformas de 32 bits funciona somente com valores HRESULT.</span><span class="sxs-lookup"><span data-stu-id="a028a-108">MAPI on 32-bit platforms works solely with HRESULT values.</span></span>
  
<span data-ttu-id="a028a-109">A ilustração a seguir mostra o formato HRESULT para plataformas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a028a-109">The following illustration shows the HRESULT format for 32-bit platforms.</span></span>
  
<span data-ttu-id="a028a-110">**HRESULT format**</span><span class="sxs-lookup"><span data-stu-id="a028a-110">**HRESULT format**</span></span>
  
<span data-ttu-id="a028a-111">![Formato HRESULT] (media/amapi_49.gif "Formato HRESULT")</span><span class="sxs-lookup"><span data-stu-id="a028a-111">![HRESULT format](media/amapi_49.gif "HRESULT format")</span></span>
  
<span data-ttu-id="a028a-112">O bit de ordem alta no HRESULT indica se o valor de retorno representa sucesso ou falha.</span><span class="sxs-lookup"><span data-stu-id="a028a-112">The high order bit in the HRESULT indicates whether the return value represents success or failure.</span></span> <span data-ttu-id="a028a-113">Se definido como zero, o valor indica sucesso.</span><span class="sxs-lookup"><span data-stu-id="a028a-113">If set to zero, the value indicates success.</span></span> <span data-ttu-id="a028a-114">Se definida como 1, indica falha.</span><span class="sxs-lookup"><span data-stu-id="a028a-114">If set to 1, it indicates failure.</span></span>
  
<span data-ttu-id="a028a-115">O R, C, N e bits r reservados no HRESULT.</span><span class="sxs-lookup"><span data-stu-id="a028a-115">The R, C, N, and r bits are reserved in the HRESULT.</span></span>
  
<span data-ttu-id="a028a-116">O campo de recurso nas duas versões indica a área de responsabilidade para o erro.</span><span class="sxs-lookup"><span data-stu-id="a028a-116">The facility field in both versions indicates the area of responsibility for the error.</span></span> <span data-ttu-id="a028a-117">Há várias instalações, mas a maioria dos erros MAPI usar FACILITY_ITF para representar os erros de interface.</span><span class="sxs-lookup"><span data-stu-id="a028a-117">There are several facilities, but the vast majority of MAPI errors use FACILITY_ITF to represent interface errors.</span></span> <span data-ttu-id="a028a-118">Os recursos mais comuns que são usados atualmente são: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC e FACILITY_STORAGE.</span><span class="sxs-lookup"><span data-stu-id="a028a-118">The most common facilities that are currently used are: FACILITY_NULL, FACILITY_ITF, FACILITY_DISPATCH, FACILITY_RPC, and FACILITY_STORAGE.</span></span> <span data-ttu-id="a028a-119">Se novas instalações forem necessárias, Microsoft aloca-las porque eles precisam ser exclusivas.</span><span class="sxs-lookup"><span data-stu-id="a028a-119">If new facilities are necessary, Microsoft allocates them because they need to be unique.</span></span> <span data-ttu-id="a028a-120">A tabela a seguir descreve os vários campos de recurso.</span><span class="sxs-lookup"><span data-stu-id="a028a-120">The following table describes the various facility fields.</span></span>
  
|<span data-ttu-id="a028a-121">Instalações</span><span class="sxs-lookup"><span data-stu-id="a028a-121">Facility</span></span>|<span data-ttu-id="a028a-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="a028a-122">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="a028a-123">FACILITY_NULL</span><span class="sxs-lookup"><span data-stu-id="a028a-123">FACILITY_NULL</span></span>  <br/> |<span data-ttu-id="a028a-124">Para obter códigos de status comuns amplamente aplicáveis como S_OK ou E_OUTOF_MEMORY; o valor for zero.</span><span class="sxs-lookup"><span data-stu-id="a028a-124">For broadly applicable common status codes such as S_OK or E_OUTOF_MEMORY; the value is zero.</span></span>  <br/> |
|<span data-ttu-id="a028a-125">FACILITY_ITF</span><span class="sxs-lookup"><span data-stu-id="a028a-125">FACILITY_ITF</span></span>  <br/> |<span data-ttu-id="a028a-126">Para a maioria dos códigos de status retornados de métodos de interface; o valor é definido pela interface.</span><span class="sxs-lookup"><span data-stu-id="a028a-126">For most status codes returned from interface methods; the value is defined by the interface.</span></span> <span data-ttu-id="a028a-127">Ou seja, os dois valores HRESULT com exatamente o mesmo valor 32-bit retornado de duas interfaces diferentes podem ter significados diferentes.</span><span class="sxs-lookup"><span data-stu-id="a028a-127">That is, two HRESULT values with exactly the same 32-bit value returned from two different interfaces might have different meanings.</span></span>  <br/> |
|<span data-ttu-id="a028a-128">FACILITY_DISPATCH</span><span class="sxs-lookup"><span data-stu-id="a028a-128">FACILITY_DISPATCH</span></span>  <br/> |<span data-ttu-id="a028a-129">Erros da interface para associação tardia [IDispatch](http://msdn.microsoft.com/en-us/library/ms221608.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a028a-129">For late binding [IDispatch](http://msdn.microsoft.com/en-us/library/ms221608.aspx) interface errors.</span></span>  <br/> |
|<span data-ttu-id="a028a-130">FACILITY_RPC</span><span class="sxs-lookup"><span data-stu-id="a028a-130">FACILITY_RPC</span></span>  <br/> |<span data-ttu-id="a028a-131">Para obter códigos de status retornados de chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="a028a-131">For status codes returned from remote procedure calls.</span></span>  <br/> |
|<span data-ttu-id="a028a-132">FACILITY_STORAGE</span><span class="sxs-lookup"><span data-stu-id="a028a-132">FACILITY_STORAGE</span></span>  <br/> |<span data-ttu-id="a028a-133">Para obter códigos de status retornados de chamadas de método [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) ou [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) relativos ao armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="a028a-133">For status codes returned from [IStorage](http://msdn.microsoft.com/en-us/library/aa380015%28VS.85%29.aspx) or [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) method calls relating to structured storage.</span></span> <span data-ttu-id="a028a-134">Códigos de status com valores de código (16 bits inferiores) nos códigos de erro de intervalo do Windows (ou seja, menos de 256) têm o mesmo significado como os erros do Windows correspondentes.</span><span class="sxs-lookup"><span data-stu-id="a028a-134">Status codes with code (lower 16 bits) values in the range of Windows error codes (that is, less than 256) have the same meaning as the corresponding Windows errors.</span></span>  <br/> |
   
<span data-ttu-id="a028a-135">O campo código é um número exclusivo atribuído para representar o erro ou aviso.</span><span class="sxs-lookup"><span data-stu-id="a028a-135">The code field is a unique number that is assigned to represent the error or warning.</span></span>
  

