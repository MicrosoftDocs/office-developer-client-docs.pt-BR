---
title: IAddrBookPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.PrepareRecips
api_type:
- COM
ms.assetid: d423f7b5-23b8-44dd-bca3-6590182dc42d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 004498ac94aadaa075d87d4dd3c675c8cd5f4feb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563874"
---
# <a name="iaddrbookpreparerecips"></a>IAddrBook::PrepareRecips

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Prepara uma lista de destinatários para uso posterior pelo sistema de mensagens. 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a entrada é aberta. O seguinte sinalizador pode ser definido:
    
MAPI_CACHE_ONLY
  
> Use somente o catálogo de endereços offline para executar a resolução de nomes. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente para abrir a lista de endereços global (GAL) no modo cache do exchange e acessar uma entrada no catálogo de endereços do cache sem criar o tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.
    
 _lpSPropTagArray_
  
> [in] Um ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade que indicam as propriedades, se houver, que requeiram a atualização. O parâmetro _lpSPropTagArray_ pode ser NULL. 
    
 _lpRecipList_
  
> [in] Um ponteiro para uma estrutura [ADRLIST](adrlist.md) que contém a lista de destinatários. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A lista de destinatários foi preparada com êxito.
    
## <a name="remarks"></a>Comentários

Clientes e provedores de serviços de chamar o método de **PrepareRecips** para fazer o seguinte: 
  
- Certifique-se de que todos os destinatários no parâmetro _lpRecipList_ tenham identificadores de entrada de longo prazo. 
    
- Certifique-se de que cada destinatário no parâmetro _lpRecipList_ tem as propriedades listadas no parâmetro _lpSPropTagArray_ e que essas propriedades serão exibidas no início da lista de destinatários. 
    
MAPI converte os identificadores de entrada de curto prazo de cada destinatário aos identificadores de entrada de longo prazo. Se necessário, longo prazo identificadores de entrada dos destinatários são recuperados do provedor de catálogo de endereço apropriado e as propriedades adicionais solicitadas.
  
Em uma entrada individual de destinatário, as propriedades solicitadas são ordenadas primeiro, seguido de quaisquer propriedades que já estavam presentes para a entrada. Se uma ou mais das propriedades solicitadas no parâmetro _lpSPropTagArray_ não são tratados pelo provedor de catálogo de endereço apropriado, seus tipos de propriedade serão definidos para PT_ERROR. Seus valores de propriedade serão definidos para a E_NOT_FOUND ou a outro valor que dá um motivo mais específico, por que as propriedades não estão disponíveis. Cada estrutura [SPropValue](spropvalue.md) incluída no parâmetro _lpRecipList_ deve ser alocada separadamente usando as funções [MAPIAllocateBuffer](mapiallocatebuffer.md) e [MAPIAllocateMore](mapiallocatemore.md) para que ela pode ser liberada individualmente. 
  
Para obter informações sobre PT_ERROR, consulte [Tipos de propriedade](property-types.md).
  
## <a name="see-also"></a>Confira também



[ADRLIST](adrlist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[Propriedade canônica PidTagEntryId](pidtagentryid-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

