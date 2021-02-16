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
  
> [in] Uma máscara de bits de sinalizadores que controla como a entrada é aberta. O sinalizador a seguir pode ser definido:
    
MAPI_CACHE_ONLY
  
> Use somente o livro de endereços offline para executar a resolução de nomes. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente abra a GAL (lista de endereços global) no modo cache do Exchange e acesse uma entrada nesse livro de endereços do cache sem criar tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas pelo Provedor de Agenda do Exchange.
    
 _lpSPropTagArray_
  
> [in] Um ponteiro para uma [estrutura SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade que indicam as propriedades, se alguma, que exigem atualização. O  _parâmetro lpSPropTagArray_ pode ser NULL. 
    
 _lpRecipList_
  
> [in] Um ponteiro para uma [estrutura ADRLIST](adrlist.md) que contém a lista de destinatários. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A lista de destinatários foi preparada com êxito.
    
## <a name="remarks"></a>Comentários

Os clientes e provedores de serviços chamam **o método PrepareRecips** para fazer o seguinte: 
  
- Verifique se todos os destinatários no  _parâmetro lpRecipList_ têm identificadores de entrada de longo prazo. 
    
- Verifique se cada destinatário no parâmetro  _lpRecipList_ tem as propriedades listadas no parâmetro  _lpSPropTagArray_ e se essas propriedades aparecem no início da lista de destinatários. 
    
O MAPI converte os identificadores de entrada de curto prazo de cada destinatário em identificadores de entrada de longo prazo. Se necessário, os identificadores de entrada de longo prazo dos destinatários são recuperados do provedor de livro de endereços apropriado e quaisquer propriedades adicionais são solicitadas.
  
Em uma entrada de destinatário individual, as propriedades solicitadas são ordenadas primeiro, seguidas por quaisquer propriedades que já estavam presentes para a entrada. Se uma ou mais das propriedades solicitadas no parâmetro  _lpSPropTagArray_ não são manipuladas pelo provedor de livro de endereços apropriado, seus tipos de propriedade serão definidos como PT_ERROR. Seus valores de propriedade serão definidos como MAPI_E_NOT_FOUND ou como outro valor que dê um motivo mais específico para as propriedades não estar disponíveis. Cada estrutura [SPropValue](spropvalue.md) incluída no parâmetro  _lpRecipList_ deve ser alocada separadamente usando as funções [MAPIAllocateBuffer](mapiallocatebuffer.md) e [MAPIAllocateMore](mapiallocatemore.md) para que possa ser liberada individualmente. 
  
Para obter informações sobre PT_ERROR, consulte [Tipos de Propriedade.](property-types.md)
  
## <a name="see-also"></a>Confira também



[ADRLIST](adrlist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[Propriedade canônica PidTagEntryId](pidtagentryid-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

