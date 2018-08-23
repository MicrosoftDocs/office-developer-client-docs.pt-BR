---
title: IABContainerResolveNames
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.ResolveNames
api_type:
- COM
ms.assetid: 27474af2-29a2-4cfb-b94f-72eb91562dac
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 81f35f659342d6258d60f40b12bd0a3ac2dc20b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588472"
---
# <a name="iabcontainerresolvenames"></a>IABContainer::ResolveNames

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Executa a resolução de nomes para uma ou mais entradas de destinatário.
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a>Par�metros

 _lpPropTagArray_
  
> [in] Um ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade descrevendo as propriedades a serem incluídos na estrutura de [ADRLIST](adrlist.md) retornada pelo provedor. Para solicitar a conjunto de propriedades padrão do provedor, passe NULL no parâmetro _lpPropTagArray_ . 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo do texto em cadeias de caracteres retornadas. Sinalizadores a seguir podem ser definidos:
    
EMS_AB_ADDRESS_LOOKUP
  
> Somente as correspondências exatas proxy endereço serão encontradas; correspondências parciais são ignoradas. Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.
    
MAPI_CACHE_ONLY
  
> Apenas o catálogo de endereços offline será usado para executar a resolução de nome. Por exemplo, você pode usar esse sinalizador para habilitar um aplicativo cliente para abrir a lista de endereços global (GAL) no modo cache do exchange e acessar uma entrada no catálogo de endereços do cache sem criar o tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange. 
    
MAPI_UNICODE 
  
> As propriedades de cadeia de caracteres retornada estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _lpAdrList_
  
> [além, out] Na entrada, um ponteiro para uma estrutura **ADRLIST** que contém a lista de destinatários para ser resolvido. Na saída, um ponteiro para uma estrutura **ADRLIST** que contém os nomes resolvidos. 
    
 _lpFlagList_
  
> [além, out] Um ponteiro para uma matriz dos sinalizadores, cada sinalizador correspondente em uma estrutura de [ADRENTRY](adrentry.md) no parâmetro _lpAdrList_ , que fornece o status da operação de resolução de nome do destinatário. Os sinalizadores no parâmetro _lpFlagList_ estão na mesma ordem como as entradas de _lpAdrList_. Sinalizadores a seguir podem ser definidos:
    
MAPI_AMBIGUOUS 
  
> O destinatário correspondente foi resolvido, mas não a um identificador exclusivo de entrada. Outros contêineres não devem tentar resolver o destinatário. 
    
MAPI_RESOLVED 
  
> O destinatário correspondente a um identificador exclusivo de entrada foi resolvido. Outros contêineres não devem tentar resolver o destinatário. 
    
MAPI_UNRESOLVED 
  
> A entrada correspondente não foi resolvida. Outros contêineres devem tentar resolver o destinatário.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O processo de resolução de nomes foi bem-sucedida.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.
    
MAPI_E_NO_SUPPORT 
  
> O provedor de catálogo de endereços não oferece suporte a resolução de nomes em massa usando esse método.
    
## <a name="remarks"></a>Comentários

O método **ResolveNames** tenta corresponder destinatários não resolvidos da matriz de entradas no parâmetro _lpAdrList_ para destinatários neste contêiner de catálogo de endereços. Um destinatário não resolvido geralmente tem apenas a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) e, possivelmente, algumas outras propriedades. Um destinatário não resolvido não tem a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) e seu sinalizador correspondente no parâmetro _lpFlagList_ estiver definido como MAPI_UNRESOLVED. Por outro lado, um destinatário resolvido sempre possui pelo menos a propriedade **PR_ENTRYID** plus várias outras propriedades como **PR_ADDRTYPE** ([ , **PR_DISPLAY_NAME**e **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) PidTagAddressType](pidtagaddresstype-canonical-property.md)).
  
Resolução de nomes geralmente inicia quando um cliente chama o método [IAddrBook::ResolveName](iaddrbook-resolvename.md) . MAPI do Outlook responde ao chamar o método **ResolveNames** de cada contêiner de catálogo de endereços incluída no caminho de pesquisa de catálogo de endereços, especificado pela propriedade **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)). As entradas no parâmetro _lpAdrList_ incluir destinatários já resolvidos porque eles são nos contêineres para o qual MAPI já chamado **ResolveNames**, pois as entradas aparecem anteriormente no caminho de pesquisa. 
  
Cada contêiner tenta resolver as entradas não resolvidas combinando o nome de exibição do destinatário com o nome de exibição de uma das suas entradas. Quando é encontrada uma correspondência exclusiva, **ResolveNames** adiciona a propriedade **PR_ENTRYID** e outras propriedades que estão incluídas no parâmetro _lpPropTagArray_ para a entrada correspondente na estrutura **ADRLIST** de saída. **ResolveNames** , em seguida, define a entrada no parâmetro _lpFlagList_ para MAPI_RESOLVED. O identificador de entrada armazenado na propriedade **PR_ENTRYID** pode ser curto ou longo prazo. 
  
Afinal dos contêineres na pesquisa caminho tentaram o processo de resolução de nome, MAPI abre uma caixa de diálogo, se possível, para solicitar ao usuário para ajudar a resolver conflitos restantes. 
  
Os clientes também podem usar a estrutura **ADRLIST** retornada em chamadas para o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Você não é necessárias para dar suporte a resolução de nomes com o método **ResolveNames** . Em vez disso, ou Além disso, você pode oferecer suporte com a restrição de propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)). Se você decidir contam com a restrição de **PR_ANR** para resolução de nome, você pode retornar MAPI_E_NO_SUPPORT. Para obter mais informações, consulte [Implementando a resolução de nome](implementing-name-resolution.md).
  
Defina a entrada de sinalizador de um destinatário no parâmetro _lpFlagList_ para MAPI_UNRESOLVED se o destinatário não corresponder a qualquer um dos destinatários do contêiner. 
  
Quando um destinatário corresponde a vários destinatários, defina seu sinalizador para MAPI_AMBIGUOUS e não altere sua estrutura **ADRENTRY** . 
  
MAPI requer determinadas propriedades para os destinatários incluídos na lista de destinatários da mensagem. Você pode incluí-las na estrutura **ADRENTRY** como parte do processo de resolução de nome ou aguarde MAPI solicitá-los com chamadas para os métodos [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) e [IMAPISupport::ExpandRecips](imapisupport-expandrecips.md) . Você pode eliminar essas chamadas extras e melhorar o desempenho, incluindo as seguintes propriedades nas estruturas **ADRENTRY** de todos os destinatários resolvidos: 
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Se algumas das propriedades no parâmetro _lpPropTagArray_ não estão disponíveis — normalmente porque a entrada de contêiner não dá suporte as propriedades e eles não são incluídos em membro **ADRENTRY** do destinatário na estrutura de **ADRLIST** — Defina o tipo de propriedade de cada propriedade não está disponível como PT_ERROR. 
  
Não remova todas as propriedades da estrutura de **ADRENTRY** do destinatário resolvido. 
  
Se você deve substituir em vez de modificar uma estrutura **ADRENTRY** , livre a estrutura original de **ADRENTRY** primeiro por chamar a função de [MAPIFreeBuffer](mapifreebuffer.md) e alocar a estrutura **ADRENTRY** com [de substituição MAPIAllocateBuffer](mapiallocatebuffer.md).
  
## <a name="see-also"></a>Confira também



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[IAddrBook::PrepareRecips](iaddrbook-preparerecips.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPISupport::ExpandRecips](imapisupport-expandrecips.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[Propriedade canônica PidTagAnr](pidtaganr-canonical-property.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)

