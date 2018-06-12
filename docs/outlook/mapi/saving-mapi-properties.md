---
title: Salvar propriedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6135dfae915a1e70743f9224352390c4b56ea02e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770287"
---
# <a name="saving-mapi-properties"></a><span data-ttu-id="59184-103">Salvar propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="59184-103">Saving MAPI Properties</span></span>

  
  
<span data-ttu-id="59184-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="59184-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="59184-105">Muitos objetos oferecem suporte a um modelo de transação de processamento por meio da qual as alterações nas propriedades não são feitas permanentes até que sejam confirmadas mais tarde.</span><span class="sxs-lookup"><span data-stu-id="59184-105">Many objects support a transaction model of processing whereby changes to properties are not made permanent until they are committed at a later time.</span></span> <span data-ttu-id="59184-106">Enquanto as alterações nas propriedades são manipuladas pelos métodos [IMAPIProp::SetProps](imapiprop-setprops.md) e [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) , a etapa de confirmação é manipulada pela [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="59184-106">Whereas changes to properties are handled by the [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) methods, the commit step is handled by [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="59184-107">Não é até depois de uma chamada bem sucedida a **SaveChanges** que a versão mais recente de propriedades de um objeto pode ser acessada.</span><span class="sxs-lookup"><span data-stu-id="59184-107">It isn't until after a successful call to **SaveChanges** that the most recent version of an object's properties can be accessed.</span></span> 
  
<span data-ttu-id="59184-108">Quando **SaveChanges** retornará o valor de erro MAPI_E_OBJECT_CHANGED, este é um aviso de que outro cliente simultaneamente é confirmar as alterações ao objeto.</span><span class="sxs-lookup"><span data-stu-id="59184-108">When **SaveChanges** returns the error value MAPI_E_OBJECT_CHANGED, this is a warning that another client is simultaneously committing changes to the object.</span></span> <span data-ttu-id="59184-109">É possível, dependendo do provedor de implementar o objeto, para que vários clientes com êxito, abra um objeto chamando o seu método de **OpenEntry** com o conjunto de sinalizador MAPI_MODIFY, concedendo a eles acesso de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="59184-109">It is possible, depending on the provider implementing the object, for multiple clients to successfully open an object by calling its **OpenEntry** method with the MAPI_MODIFY flag set, giving them read/write access.</span></span> <span data-ttu-id="59184-110">O objeto que é retornado como uma chamada **OpenEntry** é um instantâneo dos dados de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="59184-110">The object that is returned from such an **OpenEntry** call is a snapshot of the storage data.</span></span> <span data-ttu-id="59184-111">Cada tentativa subsequente para alterar esses dados pode substituir a tentativa anterior.</span><span class="sxs-lookup"><span data-stu-id="59184-111">Each subsequent attempt to change this data can overwrite the previous attempt.</span></span> 
  
<span data-ttu-id="59184-112">Ao receber MAPI_E_OBJECT_CHANGED de **SaveChanges**, um cliente tem a opção de:</span><span class="sxs-lookup"><span data-stu-id="59184-112">Upon receiving MAPI_E_OBJECT_CHANGED from **SaveChanges**, a client has the option to:</span></span> 
  
- <span data-ttu-id="59184-113">Fazer uma cópia do objeto para armazenar as alterações.</span><span class="sxs-lookup"><span data-stu-id="59184-113">Make a copy of the object to hold the changes.</span></span>
    
- <span data-ttu-id="59184-114">Fazer outra chamada para **SaveChanges**, especificando FORCE_SAVE.</span><span class="sxs-lookup"><span data-stu-id="59184-114">Make another call to **SaveChanges**, specifying FORCE_SAVE.</span></span> 
    
<span data-ttu-id="59184-115">Chamar **SaveChanges** com o sinalizador FORCE_SAVE substitui o salvamento anterior e torna permanentes as alterações de um cliente.</span><span class="sxs-lookup"><span data-stu-id="59184-115">Calling **SaveChanges** with the FORCE_SAVE flag overwrites the previous save and makes a client's changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="59184-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="59184-116">See also</span></span>



[<span data-ttu-id="59184-117">Vis�o geral da propriedade MAPI</span><span class="sxs-lookup"><span data-stu-id="59184-117">MAPI Property Overview</span></span>](mapi-property-overview.md)

