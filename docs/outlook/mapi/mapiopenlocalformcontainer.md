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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427735"
---
# <a name="mapiopenlocalformcontainer"></a><span data-ttu-id="2c447-103">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="2c447-103">MAPIOpenLocalFormContainer</span></span>

  
  
<span data-ttu-id="2c447-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c447-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c447-105">Retorna um ponteiro de interface para a biblioteca de formulário local.</span><span class="sxs-lookup"><span data-stu-id="2c447-105">Returns an interface pointer to the local form library.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2c447-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2c447-106">Header file:</span></span>  <br/> |<span data-ttu-id="2c447-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="2c447-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="2c447-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="2c447-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2c447-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2c447-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2c447-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="2c447-110">Called by:</span></span>  <br/> |<span data-ttu-id="2c447-111">Aplicativos do cliente</span><span class="sxs-lookup"><span data-stu-id="2c447-111">Client applications</span></span>  <br/> |
   
```cpp
MAPIOpenLocalFormContainer(
  LPMAPIFORMCONTAINER FAR * ppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="2c447-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2c447-112">Parameters</span></span>

 <span data-ttu-id="2c447-113">_ppfcnt_</span><span class="sxs-lookup"><span data-stu-id="2c447-113">_ppfcnt_</span></span>
  
> <span data-ttu-id="2c447-114">[out] Ponteiro para um ponteiro para a interface da biblioteca de formulário local.</span><span class="sxs-lookup"><span data-stu-id="2c447-114">[out] Pointer to a pointer to the local form library interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2c447-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2c447-115">Return value</span></span>

<span data-ttu-id="2c447-116">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2c447-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2c447-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c447-117">Remarks</span></span>

<span data-ttu-id="2c447-118">A interface para a qual um ponteiro é retornado pode ser usada por programas de instalação de terceiros para instalar formulários específicos do aplicativo na biblioteca sem que o programa primeiro tenha que fazer logoff no MAPI.</span><span class="sxs-lookup"><span data-stu-id="2c447-118">The interface to which a pointer is returned can be used by third-party installation programs to install application-specific forms into the library without the program first having to log on to MAPI.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2c447-119">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2c447-119">MFCMAPI reference</span></span>

<span data-ttu-id="2c447-120">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2c447-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2c447-121">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="2c447-121">**File**</span></span>|<span data-ttu-id="2c447-122">**Função**</span><span class="sxs-lookup"><span data-stu-id="2c447-122">**Function**</span></span>|<span data-ttu-id="2c447-123">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="2c447-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2c447-124">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="2c447-124">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="2c447-125">CMainDlg::OnMAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="2c447-125">CMainDlg::OnMAPIOpenLocalFormContainer</span></span>  <br/> |<span data-ttu-id="2c447-126">MFCMAPI usa o **método MAPIOpenLocalFormContainer** para abrir o contêiner de formulário local para renderizar em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="2c447-126">MFCMAPI uses the **MAPIOpenLocalFormContainer** method to open the local form container to render in a new window.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2c447-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="2c447-127">See also</span></span>



[<span data-ttu-id="2c447-128">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="2c447-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

