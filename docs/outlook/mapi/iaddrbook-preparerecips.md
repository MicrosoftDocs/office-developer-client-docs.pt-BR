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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: db1c23f33e604d6aafdd8a046566c7390c281ad8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414274"
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
  
> no Uma bitmask de sinalizadores que controla como a entrada é aberta. O seguinte sinalizador pode ser definido:
    
MAPI_CACHE_ONLY
  
> Use apenas o catálogo de endereços offline para executar a resolução de nomes. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente Abra a lista de endereços global (GAL) no modo cache do Exchange e acesse uma entrada desse catálogo de endereços do cache sem criar tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.
    
 _lpSPropTagArray_
  
> no Um ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade que indicam as propriedades, se houver, que precisam de atualização. O parâmetro _lpSPropTagArray_ pode ser NULL. 
    
 _lpRecipList_
  
> no Um ponteiro para uma estrutura [das ADRLIST](adrlist.md) que contém a lista de destinatários. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A lista de destinatários foi preparada com êxito.
    
## <a name="remarks"></a>Comentários

Os clientes e os provedores de serviços chamam o método **PrepareRecips** para fazer o seguinte: 
  
- Certifique-se de que todos os destinatários no parâmetro _lpRecipList_ tenham identificadores de entrada de longo prazo. 
    
- Certifique-se de que cada destinatário no parâmetro _lpRecipList_ tenha as propriedades listadas no parâmetro _lpSPropTagArray_ e que essas propriedades apareçam no início da lista de destinatários. 
    
MAPI converte os identificadores de entrada de curto prazo de cada destinatário em identificadores de entrada de longo prazo. Se necessário, os identificadores de entrada de longo prazo dos destinatários são recuperados do provedor de catálogo de endereços apropriado e qualquer propriedade adicional é solicitada.
  
Em uma entrada de destinatário individual, as propriedades solicitadas são ordenadas primeiro, seguidas por qualquer propriedade que já estava presente para a entrada. Se uma ou mais das propriedades solicitadas no parâmetro _lpSPropTagArray_ não forem tratadas pelo provedor de catálogo de endereços apropriado, seus tipos de propriedade serão definidos como PT_ERROR. Seus valores de propriedade serão definidos para MAPI_E_NOT_FOUND ou para outro valor que forneça um motivo mais específico para que as propriedades não estejam disponíveis. Cada estrutura [SPropValue](spropvalue.md) incluída no parâmetro _lpRecipList_ deve ser alocada separadamente usando as funções [MAPIAllocateBuffer](mapiallocatebuffer.md) e [MAPIAllocateMore](mapiallocatemore.md) para que ela possa ser liberada individualmente. 
  
Para obter informações sobre o PT_ERROR, consulte [tipos de propriedade](property-types.md).
  
## <a name="see-also"></a>Confira também



[ADRLIST](adrlist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[Propriedade canônica PidTagEntryId](pidtagentryid-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

