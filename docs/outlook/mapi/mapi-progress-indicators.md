---
title: Indicadores de progresso MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8fc39c6d7da0970ee15cdd9dd67bfeef0997d7d1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582865"
---
# <a name="mapi-progress-indicators"></a><span data-ttu-id="ef437-103">Indicadores de progresso MAPI</span><span class="sxs-lookup"><span data-stu-id="ef437-103">MAPI Progress Indicators</span></span>

  
  
<span data-ttu-id="ef437-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef437-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef437-105">Muitas das operações que podem ser executadas para clientes podem levar muito tempo para ser concluída.</span><span class="sxs-lookup"><span data-stu-id="ef437-105">Many of the operations that you perform for clients can take a long time to complete.</span></span> <span data-ttu-id="ef437-106">Para informar aos clientes sobre o progresso de uma operação demorada, você pode mostrar um indicador que exibe graficamente a terminar parte de uma operação em qualquer ponto do início da operação para sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="ef437-106">To inform clients of the progress of a lengthy operation, you can show an indicator that displays graphically the finished portion of an operation at any given point from the start of the operation to its completion.</span></span> <span data-ttu-id="ef437-107">O indicador de progresso mostra uma porcentagem do total a operação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="ef437-107">The progress indicator shows a percentage of the total operation to be completed.</span></span>
  
<span data-ttu-id="ef437-108">Os seguintes métodos suportam operações demoradas e a exibição de um indicador de progresso:</span><span class="sxs-lookup"><span data-stu-id="ef437-108">The following methods support lengthy operations and the display of a progress indicator:</span></span>
  
- <span data-ttu-id="ef437-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md)e [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span><span class="sxs-lookup"><span data-stu-id="ef437-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md), and [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span>
    
- <span data-ttu-id="ef437-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) e [IMAPIProp::CopyTo](imapiprop-copyto.md).</span><span class="sxs-lookup"><span data-stu-id="ef437-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md).</span></span>
    
- <span data-ttu-id="ef437-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md)e [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span><span class="sxs-lookup"><span data-stu-id="ef437-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md), and [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span></span>
    
- <span data-ttu-id="ef437-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span><span class="sxs-lookup"><span data-stu-id="ef437-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span></span>
    
- <span data-ttu-id="ef437-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span><span class="sxs-lookup"><span data-stu-id="ef437-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span></span>
    
<span data-ttu-id="ef437-114">Para exibir um indicador de progresso, MAPI define um objeto de andamento.</span><span class="sxs-lookup"><span data-stu-id="ef437-114">To display a progress indicator, MAPI defines a progress object.</span></span> <span data-ttu-id="ef437-115">Objetos de progresso implementar o [IMAPIProgress: IUnknown](imapiprogressiunknown.md) interface, uma interface que inclui métodos para estabelecer o intervalo do indicador e criando a exibição.</span><span class="sxs-lookup"><span data-stu-id="ef437-115">Progress objects implement the [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface, an interface that includes methods for establishing the range of the indicator and creating the display.</span></span> <span data-ttu-id="ef437-116">MAPI fornece uma implementação de objeto de progresso como alguns clientes.</span><span class="sxs-lookup"><span data-stu-id="ef437-116">MAPI provides a progress object implementation as do some clients.</span></span> <span data-ttu-id="ef437-117">Você deve usar a implementação de um cliente, se esta for fornecida, como um parâmetro de entrada para o método executar a operação.</span><span class="sxs-lookup"><span data-stu-id="ef437-117">You should use a client's implementation, if one is supplied, as an input parameter to the method performing the operation.</span></span> <span data-ttu-id="ef437-118">Se o cliente passa NULL em vez de um ponteiro para um objeto de andamento, use a implementação de MAPI chamando o método [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="ef437-118">If the client passes NULL instead of a pointer to a progress object, use MAPI's implementation by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ef437-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef437-119">See also</span></span>



[<span data-ttu-id="ef437-120">Provedores de serviços MAPI</span><span class="sxs-lookup"><span data-stu-id="ef437-120">MAPI Service Providers</span></span>](mapi-service-providers.md)

