---
title: MAPIOpenLocalFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIOpenLocalFormContainer
api_type:
- COM
ms.assetid: 1c53170f-03a6-4a05-913e-de8eeadea692
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c00c2fa04ae7e89f8c23c085ba021a935748ad4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768015"
---
# <a name="mapiopenlocalformcontainer"></a><span data-ttu-id="ac5ae-103">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="ac5ae-103">MAPIOpenLocalFormContainer</span></span>

  
  
<span data-ttu-id="ac5ae-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ac5ae-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ac5ae-105">Retorna um ponteiro de interface para a biblioteca de formulários local.</span><span class="sxs-lookup"><span data-stu-id="ac5ae-105">Returns an interface pointer to the local form library.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ac5ae-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ac5ae-106">Header file:</span></span>  <br/> |<span data-ttu-id="ac5ae-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="ac5ae-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="ac5ae-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="ac5ae-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ac5ae-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ac5ae-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ac5ae-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="ac5ae-110">Called by:</span></span>  <br/> |<span data-ttu-id="ac5ae-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="ac5ae-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="ac5ae-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac5ae-112">Parameters</span></span>

 <span data-ttu-id="ac5ae-113">_ppfcnt_</span><span class="sxs-lookup"><span data-stu-id="ac5ae-113">_ppfcnt_</span></span>
  
> <span data-ttu-id="ac5ae-114">[out] Ponteiro para um ponteiro para a interface de biblioteca de formulários locais.</span><span class="sxs-lookup"><span data-stu-id="ac5ae-114">[out] Pointer to a pointer to the local form library interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ac5ae-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ac5ae-115">Return value</span></span>

<span data-ttu-id="ac5ae-116">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="ac5ae-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ac5ae-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac5ae-117">Remarks</span></span>

<span data-ttu-id="ac5ae-118">A interface para o qual um ponteiro é retornado pode ser usada por programas de instalação de terceiros para instalar formulários de aplicativo específico para a biblioteca sem o programa primeiro precisar fazer logon no MAPI.</span><span class="sxs-lookup"><span data-stu-id="ac5ae-118">The interface to which a pointer is returned can be used by third-party installation programs to install application-specific forms into the library without the program first having to log on to MAPI.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ac5ae-119">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ac5ae-119">MFCMAPI reference</span></span>

<span data-ttu-id="ac5ae-120">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ac5ae-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ac5ae-121">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ac5ae-121">**File**</span></span>|<span data-ttu-id="ac5ae-122">**Function**</span><span class="sxs-lookup"><span data-stu-id="ac5ae-122">**Function**</span></span>|<span data-ttu-id="ac5ae-123">**Comment**</span><span class="sxs-lookup"><span data-stu-id="ac5ae-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ac5ae-124">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="ac5ae-124">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="ac5ae-125">CMainDlg::OnMAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="ac5ae-125">CMainDlg::OnMAPIOpenLocalFormContainer</span></span>  <br/> |<span data-ttu-id="ac5ae-126">MFCMAPI usa o método **MAPIOpenLocalFormContainer** para abrir o contêiner de formulário local para renderizar em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="ac5ae-126">MFCMAPI uses the **MAPIOpenLocalFormContainer** method to open the local form container to render in a new window.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ac5ae-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac5ae-127">See also</span></span>



[<span data-ttu-id="ac5ae-128">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="ac5ae-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

