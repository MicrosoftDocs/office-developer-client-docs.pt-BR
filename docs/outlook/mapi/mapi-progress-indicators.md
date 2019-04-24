---
title: Indicadores de progresso MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 73a99e52-97fe-40f5-af90-52cfd858ab22
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: cdfb6898146583b7da9b043eadd3acc09edbf292
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328207"
---
# <a name="mapi-progress-indicators"></a><span data-ttu-id="e1e85-103">Indicadores de progresso MAPI</span><span class="sxs-lookup"><span data-stu-id="e1e85-103">MAPI Progress Indicators</span></span>

  
  
<span data-ttu-id="e1e85-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1e85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1e85-105">Muitas das operações que você realiza para os clientes podem levar muito tempo para serem concluídas.</span><span class="sxs-lookup"><span data-stu-id="e1e85-105">Many of the operations that you perform for clients can take a long time to complete.</span></span> <span data-ttu-id="e1e85-106">Para informar os clientes sobre o progresso de uma operação extensa, você pode mostrar um indicador que exibe graficamente a parte concluída de uma operação em um determinado ponto, desde o início da operação até sua conclusão.</span><span class="sxs-lookup"><span data-stu-id="e1e85-106">To inform clients of the progress of a lengthy operation, you can show an indicator that displays graphically the finished portion of an operation at any given point from the start of the operation to its completion.</span></span> <span data-ttu-id="e1e85-107">O indicador de progresso mostra uma porcentagem da operação total a ser concluída.</span><span class="sxs-lookup"><span data-stu-id="e1e85-107">The progress indicator shows a percentage of the total operation to be completed.</span></span>
  
<span data-ttu-id="e1e85-108">Os seguintes métodos suportam operações demoradas e a exibição de um indicador de progresso:</span><span class="sxs-lookup"><span data-stu-id="e1e85-108">The following methods support lengthy operations and the display of a progress indicator:</span></span>
  
- <span data-ttu-id="e1e85-109">[IMAPIFolder:: CopyMessages](imapifolder-copymessages.md), [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::D Eletemessages](imapifolder-deletemessages.md), [IMAPIFolder::D Eletefolder](imapifolder-deletefolder.md), [IMAPIFolder:: EmptyFolder](imapifolder-emptyfolder.md)e [IMAPIFolder:](imapifolder-setreadflags.md): SetReadFlags.</span><span class="sxs-lookup"><span data-stu-id="e1e85-109">[IMAPIFolder::CopyMessages](imapifolder-copymessages.md), [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md), [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md), [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md), [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md), and [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md).</span></span>
    
- <span data-ttu-id="e1e85-110">[IMAPIProp:: CopyProps](imapiprop-copyprops.md) e [IMAPIProp:: CopyTo](imapiprop-copyto.md).</span><span class="sxs-lookup"><span data-stu-id="e1e85-110">[IMAPIProp::CopyProps](imapiprop-copyprops.md) and [IMAPIProp::CopyTo](imapiprop-copyto.md).</span></span>
    
- <span data-ttu-id="e1e85-111">[IMAPISupport::D ocopyprops](imapisupport-docopyprops.md), [IMAPISupport::D ocopyto](imapisupport-docopyto.md), [IMAPISupport:: CopyFolder](imapisupport-copyfolder.md)e [IMAPISupport::](imapisupport-copymessages.md)CopyMessages.</span><span class="sxs-lookup"><span data-stu-id="e1e85-111">[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md), [IMAPISupport::DoCopyTo](imapisupport-docopyto.md), [IMAPISupport::CopyFolder](imapisupport-copyfolder.md), and [IMAPISupport::CopyMessages](imapisupport-copymessages.md).</span></span>
    
- <span data-ttu-id="e1e85-112">[IMessage::D eleteattach](imessage-deleteattach.md).</span><span class="sxs-lookup"><span data-stu-id="e1e85-112">[IMessage::DeleteAttach](imessage-deleteattach.md).</span></span>
    
- <span data-ttu-id="e1e85-113">[IABContainer:: CopyEntries](iabcontainer-copyentries.md).</span><span class="sxs-lookup"><span data-stu-id="e1e85-113">[IABContainer::CopyEntries](iabcontainer-copyentries.md).</span></span>
    
<span data-ttu-id="e1e85-114">Para exibir um indicador de progresso, o MAPI define um objeto Progress.</span><span class="sxs-lookup"><span data-stu-id="e1e85-114">To display a progress indicator, MAPI defines a progress object.</span></span> <span data-ttu-id="e1e85-115">Os objetos Progress implementam a interface [método imapiprogress: IUnknown](imapiprogressiunknown.md) , uma interface que inclui métodos para o estabelecimento do intervalo do indicador e a criação da exibição.</span><span class="sxs-lookup"><span data-stu-id="e1e85-115">Progress objects implement the [IMAPIProgress : IUnknown](imapiprogressiunknown.md) interface, an interface that includes methods for establishing the range of the indicator and creating the display.</span></span> <span data-ttu-id="e1e85-116">O MAPI fornece uma implementação de objeto Progress como alguns clientes.</span><span class="sxs-lookup"><span data-stu-id="e1e85-116">MAPI provides a progress object implementation as do some clients.</span></span> <span data-ttu-id="e1e85-117">Você deve usar a implementação de um cliente, se um for fornecido, como um parâmetro de entrada para o método executando a operação.</span><span class="sxs-lookup"><span data-stu-id="e1e85-117">You should use a client's implementation, if one is supplied, as an input parameter to the method performing the operation.</span></span> <span data-ttu-id="e1e85-118">Se o cliente passar NULL em vez de um ponteiro para um objeto Progress, use a implementação do MAPI chamando o método [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="e1e85-118">If the client passes NULL instead of a pointer to a progress object, use MAPI's implementation by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e1e85-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1e85-119">See also</span></span>



[<span data-ttu-id="e1e85-120">Provedores de serviço MAPI</span><span class="sxs-lookup"><span data-stu-id="e1e85-120">MAPI Service Providers</span></span>](mapi-service-providers.md)

