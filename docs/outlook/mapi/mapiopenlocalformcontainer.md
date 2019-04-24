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
ms.openlocfilehash: ace31079c51aac169f6091af0cb363e7f05f0d14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270144"
---
# <a name="mapiopenlocalformcontainer"></a><span data-ttu-id="b036f-103">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="b036f-103">MAPIOpenLocalFormContainer</span></span>

  
  
<span data-ttu-id="b036f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b036f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b036f-105">Retorna um ponteiro de interface para a biblioteca de formulários local.</span><span class="sxs-lookup"><span data-stu-id="b036f-105">Returns an interface pointer to the local form library.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b036f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b036f-106">Header file:</span></span>  <br/> |<span data-ttu-id="b036f-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="b036f-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="b036f-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="b036f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b036f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b036f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b036f-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="b036f-110">Called by:</span></span>  <br/> |<span data-ttu-id="b036f-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="b036f-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="b036f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b036f-112">Parameters</span></span>

 <span data-ttu-id="b036f-113">_ppfcnt_</span><span class="sxs-lookup"><span data-stu-id="b036f-113">_ppfcnt_</span></span>
  
> <span data-ttu-id="b036f-114">bota Ponteiro para um ponteiro para a interface de biblioteca de formulários local.</span><span class="sxs-lookup"><span data-stu-id="b036f-114">[out] Pointer to a pointer to the local form library interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b036f-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b036f-115">Return value</span></span>

<span data-ttu-id="b036f-116">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="b036f-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b036f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b036f-117">Remarks</span></span>

<span data-ttu-id="b036f-118">A interface para a qual um ponteiro é retornado pode ser usada por programas de instalação de terceiros para instalar formulários específicos do aplicativo na biblioteca sem que o programa primeiro tenha que fazer logon no MAPI.</span><span class="sxs-lookup"><span data-stu-id="b036f-118">The interface to which a pointer is returned can be used by third-party installation programs to install application-specific forms into the library without the program first having to log on to MAPI.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b036f-119">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b036f-119">MFCMAPI reference</span></span>

<span data-ttu-id="b036f-120">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b036f-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b036f-121">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="b036f-121">**File**</span></span>|<span data-ttu-id="b036f-122">**Função**</span><span class="sxs-lookup"><span data-stu-id="b036f-122">**Function**</span></span>|<span data-ttu-id="b036f-123">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="b036f-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b036f-124">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="b036f-124">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="b036f-125">CMainDlg:: OnMAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="b036f-125">CMainDlg::OnMAPIOpenLocalFormContainer</span></span>  <br/> |<span data-ttu-id="b036f-126">MFCMAPI usa o método **MAPIOpenLocalFormContainer** para abrir o contêiner de formulário local para renderizar em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="b036f-126">MFCMAPI uses the **MAPIOpenLocalFormContainer** method to open the local form container to render in a new window.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b036f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="b036f-127">See also</span></span>



[<span data-ttu-id="b036f-128">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="b036f-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

