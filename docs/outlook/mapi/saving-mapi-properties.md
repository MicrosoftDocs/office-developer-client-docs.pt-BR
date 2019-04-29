---
title: Salvar propriedades MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5d4653492028151d7e19a5d5490c8c8949002a4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425887"
---
# <a name="saving-mapi-properties"></a><span data-ttu-id="4f80d-103">Salvar propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4f80d-103">Saving MAPI Properties</span></span>

  
  
<span data-ttu-id="4f80d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f80d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f80d-105">Muitos objetos dão suporte a um modelo de transação de processamento em que as alterações feitas nas propriedades não são permanentes até que sejam confirmadas posteriormente.</span><span class="sxs-lookup"><span data-stu-id="4f80d-105">Many objects support a transaction model of processing whereby changes to properties are not made permanent until they are committed at a later time.</span></span> <span data-ttu-id="4f80d-106">Enquanto as alterações nas propriedades são tratadas pelos métodos [IMAPIProp::](imapiprop-setprops.md) SetProps e [IMAPIProp::D eleteprops](imapiprop-deleteprops.md) , a etapa de confirmação é manipulada por [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="4f80d-106">Whereas changes to properties are handled by the [IMAPIProp::SetProps](imapiprop-setprops.md) and [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) methods, the commit step is handled by [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="4f80d-107">Ele não é até após uma chamada bem-sucedida para **SaveChanges** que a versão mais recente das propriedades de um objeto pode ser acessada.</span><span class="sxs-lookup"><span data-stu-id="4f80d-107">It isn't until after a successful call to **SaveChanges** that the most recent version of an object's properties can be accessed.</span></span> 
  
<span data-ttu-id="4f80d-108">Quando **SaveChanges** retorna o valor de erro MAPI_E_OBJECT_CHANGED, este é um aviso de que outro cliente está simultaneamente confirmando alterações no objeto.</span><span class="sxs-lookup"><span data-stu-id="4f80d-108">When **SaveChanges** returns the error value MAPI_E_OBJECT_CHANGED, this is a warning that another client is simultaneously committing changes to the object.</span></span> <span data-ttu-id="4f80d-109">É possível, dependendo do provedor que está implementando o objeto, para que vários clientes Abram com êxito um objeto chamando seu método **OpenEntry** com o sinalizador MAPI_MODIFY definido, concedendo a eles acesso de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4f80d-109">It is possible, depending on the provider implementing the object, for multiple clients to successfully open an object by calling its **OpenEntry** method with the MAPI_MODIFY flag set, giving them read/write access.</span></span> <span data-ttu-id="4f80d-110">O objeto que é retornado de uma chamada **OpenEntry** é um instantâneo dos dados de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4f80d-110">The object that is returned from such an **OpenEntry** call is a snapshot of the storage data.</span></span> <span data-ttu-id="4f80d-111">Cada tentativa subsequente de alterar esses dados pode substituir a tentativa anterior.</span><span class="sxs-lookup"><span data-stu-id="4f80d-111">Each subsequent attempt to change this data can overwrite the previous attempt.</span></span> 
  
<span data-ttu-id="4f80d-112">Após receber MAPI_E_OBJECT_CHANGED de **SaveChanges**, um cliente tem a opção de:</span><span class="sxs-lookup"><span data-stu-id="4f80d-112">Upon receiving MAPI_E_OBJECT_CHANGED from **SaveChanges**, a client has the option to:</span></span> 
  
- <span data-ttu-id="4f80d-113">Faça uma cópia do objeto para armazenar as alterações.</span><span class="sxs-lookup"><span data-stu-id="4f80d-113">Make a copy of the object to hold the changes.</span></span>
    
- <span data-ttu-id="4f80d-114">Faça outra chamada para **SaveChanges**, especificando FORCE_SAVE.</span><span class="sxs-lookup"><span data-stu-id="4f80d-114">Make another call to **SaveChanges**, specifying FORCE_SAVE.</span></span> 
    
<span data-ttu-id="4f80d-115">Chamar o **SaveChanges** com o sinalizador FORCE_SAVE substitui o salvamento anterior e torna as alterações de um cliente permanentes.</span><span class="sxs-lookup"><span data-stu-id="4f80d-115">Calling **SaveChanges** with the FORCE_SAVE flag overwrites the previous save and makes a client's changes permanent.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4f80d-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f80d-116">See also</span></span>



[<span data-ttu-id="4f80d-117">Visão geral da propriedade MAPI</span><span class="sxs-lookup"><span data-stu-id="4f80d-117">MAPI Property Overview</span></span>](mapi-property-overview.md)

