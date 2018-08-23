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
ms.openlocfilehash: 87696ceea96bd2f51bfe5a0b062499946179c8b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582557"
---
# <a name="mapiopenlocalformcontainer"></a><span data-ttu-id="2012d-103">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="2012d-103">MAPIOpenLocalFormContainer</span></span>

  
  
<span data-ttu-id="2012d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2012d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2012d-105">Retorna um ponteiro de interface para a biblioteca de formulários local.</span><span class="sxs-lookup"><span data-stu-id="2012d-105">Returns an interface pointer to the local form library.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2012d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2012d-106">Header file:</span></span>  <br/> |<span data-ttu-id="2012d-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="2012d-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="2012d-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="2012d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2012d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2012d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2012d-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="2012d-110">Called by:</span></span>  <br/> |<span data-ttu-id="2012d-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="2012d-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="2012d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2012d-112">Parameters</span></span>

 <span data-ttu-id="2012d-113">_ppfcnt_</span><span class="sxs-lookup"><span data-stu-id="2012d-113">_ppfcnt_</span></span>
  
> <span data-ttu-id="2012d-114">[out] Ponteiro para um ponteiro para a interface de biblioteca de formulários locais.</span><span class="sxs-lookup"><span data-stu-id="2012d-114">[out] Pointer to a pointer to the local form library interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2012d-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2012d-115">Return value</span></span>

<span data-ttu-id="2012d-116">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2012d-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2012d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2012d-117">Remarks</span></span>

<span data-ttu-id="2012d-118">A interface para o qual um ponteiro é retornado pode ser usada por programas de instalação de terceiros para instalar formulários de aplicativo específico para a biblioteca sem o programa primeiro precisar fazer logon no MAPI.</span><span class="sxs-lookup"><span data-stu-id="2012d-118">The interface to which a pointer is returned can be used by third-party installation programs to install application-specific forms into the library without the program first having to log on to MAPI.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2012d-119">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2012d-119">MFCMAPI reference</span></span>

<span data-ttu-id="2012d-120">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2012d-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2012d-121">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="2012d-121">**File**</span></span>|<span data-ttu-id="2012d-122">**Function**</span><span class="sxs-lookup"><span data-stu-id="2012d-122">**Function**</span></span>|<span data-ttu-id="2012d-123">**Comment**</span><span class="sxs-lookup"><span data-stu-id="2012d-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2012d-124">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="2012d-124">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="2012d-125">CMainDlg::OnMAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="2012d-125">CMainDlg::OnMAPIOpenLocalFormContainer</span></span>  <br/> |<span data-ttu-id="2012d-126">MFCMAPI usa o método **MAPIOpenLocalFormContainer** para abrir o contêiner de formulário local para renderizar em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="2012d-126">MFCMAPI uses the **MAPIOpenLocalFormContainer** method to open the local form container to render in a new window.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2012d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="2012d-127">See also</span></span>



[<span data-ttu-id="2012d-128">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="2012d-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

