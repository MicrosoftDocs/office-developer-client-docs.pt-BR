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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fac4978bef94650f85ac3179acd3858602f933ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279567"
---
# <a name="iabcontainerresolvenames"></a>IABContainer::ResolveNames

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Executa a resolução de nome para uma ou mais entradas de destinatário.
  
```cpp
HRESULT ResolveNames(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  LPADRLIST lpAdrList,
  LPFlagList lpFlagList
);
```

## <a name="parameters"></a>Parâmetros

 _lpPropTagArray_
  
> no Um ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade descrevendo as propriedades a serem incluídas na estrutura [das ADRLIST](adrlist.md) retornada pelo provedor. Para solicitar o conjunto de propriedades padrão do provedor, passe NULL no parâmetro _lpPropTagArray_ . 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla o tipo de texto nas cadeias de caracteres retornadas. Os seguintes sinalizadores podem ser definidos:
    
EMS_AB_ADDRESS_LOOKUP
  
> Serão encontradas apenas as correspondências exatas de endereços de proxy. as correspondências parciais são ignoradas. Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.
    
MAPI_CACHE_ONLY
  
> Somente o catálogo de endereços offline será usado para executar a resolução de nomes. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente Abra a lista de endereços global (GAL) no modo cache do Exchange e acesse uma entrada desse catálogo de endereços do cache sem criar tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange. 
    
MAPI_UNICODE 
  
> As propriedades de cadeia de caracteres retornadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.
    
 _lpAdrList_
  
> [in, out] Na entrada, um ponteiro para uma estrutura **das ADRLIST** que contém a lista de destinatários a serem resolvidos. Na saída, um ponteiro para uma estrutura **das ADRLIST** que contém os nomes resolvidos. 
    
 _lpFlagList_
  
> [in, out] Um ponteiro para uma matriz de sinalizadores, cada sinalizador correspondente a uma estrutura [ADRENTRY](adrentry.md) no parâmetro _lpAdrList_ , que fornece o status da operação de resolução de nome para o destinatário. Os sinalizadores no parâmetro _lpFlagList_ estão na mesma ordem das entradas no _lpAdrList_. Os seguintes sinalizadores podem ser definidos:
    
MAPI_AMBIGUOUS 
  
> O destinatário correspondente foi resolvido, mas não a um identificador de entrada exclusivo. Outros contêineres não devem tentar resolver esse destinatário. 
    
MAPI_RESOLVED 
  
> O destinatário correspondente foi resolvido para um identificador de entrada exclusivo. Outros contêineres não devem tentar resolver esse destinatário. 
    
MAPI_UNRESOLVED 
  
> A entrada correspondente não foi resolvida. Outros contêineres devem tentar resolver esse destinatário.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O processo de resolução de nomes foi bem-sucedido.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.
    
MAPI_E_NO_SUPPORT 
  
> O provedor de catálogo de endereços não dá suporte à resolução de nomes em massa usando esse método.
    
## <a name="remarks"></a>Comentários

O **** método ResolveNames tenta coincidir destinatários não resolvidos da matriz de entradas no parâmetro _lpAdrList_ para destinatários neste contêiner de catálogo de endereços. Normalmente, um destinatário não resolvido tem apenas a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) e, possivelmente, algumas outras propriedades. Um destinatário não resolvido não tem a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), e seu sinalizador correspondente no parâmetro _lpFlagList_ está definido como MAPI_UNRESOLVED. Por outro lado, um destinatário resolvido sempre tem pelo menos a propriedade **PR_ENTRYID** mais várias outras propriedades, como **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME**e **PR_ADDRTYPE** ([ PidTagAddressType](pidtagaddresstype-canonical-property.md)).
  
A resolução de nome normalmente começa quando um cliente chama o método [IAddrBook:: ResolveName](iaddrbook-resolvename.md) . O MAPI do Outlook responde chamando **** o método ResolveNames de cada contêiner de catálogo de endereços incluído no caminho de pesquisa do catálogo de endereços, especificado pela propriedade **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)). As entradas no parâmetro _lpAdrList_ incluem destinatários já resolvidos porque estão em contêineres para os quais o MAPI já **** chamou ResolveNames, porque as entradas aparecem anteriormente no caminho de pesquisa. 
  
Cada contêiner tenta resolver as entradas não resolvidas combinando o nome de exibição do destinatário com o nome de exibição de uma de suas entradas. Quando uma correspondência exclusiva é encontrada, **ResolveNames** adiciona a propriedade **PR_ENTRYID** e outras propriedades que são incluídas no parâmetro _lpPropTagArray_ para a entrada correspondente na estrutura **das ADRLIST** de saída. **ResolveNames** define a entrada no parâmetro _lpFlagList_ como MAPI_RESOLVED. O identificador de entrada armazenado na propriedade **PR_ENTRYID** pode ser de curto ou de longo prazo. 
  
Após todos os contêineres no caminho de pesquisa terem tentado o processo de resolução de nomes, o MAPI abre uma caixa de diálogo, se possível, para solicitar ao usuário ajuda na resolução de qualquer conflito restante. 
  
Os clientes também podem usar a estrutura **das ADRLIST** retornada em chamadas para o método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) . 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Não é necessário oferecer suporte à resolução de nomes com **** o método ResolveNames. Em vez disso, ou Adicionalmente, você pode dar suporte a ela com a restrição de propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)). Se você decidir confiar na restrição **PR_ANR** para resolução de nomes, poderá retornar MAPI_E_NO_SUPPORT. Para obter mais informações, consulte [implementaNdo resolução de nomes](implementing-name-resolution.md).
  
Defina a entrada de sinalizador de um destinatário no parâmetro _lpFlagList_ como MAPI_UNRESOLVED se o destinatário não corresponder a qualquer um dos destinatários do contêiner. 
  
Quando um destinatário corresponder a vários destinatários, defina seu sinalizador como MAPI_AMBIGUOUS e não altere sua estrutura de **ADRENTRY** . 
  
MAPI requer determinadas propriedades para destinatários incluídos na lista de destinatários de uma mensagem. Você pode incluí-los na estrutura **ADRENTRY** como parte do processo de resolução de nome ou aguardar o MAPI solicitá-los com chamadas para os métodos [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) e [IMAPISupport:: ExpandRecips](imapisupport-expandrecips.md) . Você pode eliminar essas chamadas extras e melhorar o desempenho, incluindo as seguintes propriedades nas estruturas **ADRENTRY** de todos os destinatários resolvidos: 
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Se algumas das propriedades no parâmetro _lpPropTagArray_ não estiverem disponíveis, geralmente porque a entrada de contêiner não é compatível com as propriedades e elas não estão incluídas no membro **ADRENTRY** do destinatário na estrutura **das ADRLIST** , Defina o tipo de propriedade de cada propriedade não disponível como PT_ERROR. 
  
Não remova as propriedades da estrutura **ADRENTRY** de um destinatário resolvido. 
  
Se você precisar substituir em vez de modificar uma estrutura **ADRENTRY** , libere primeiro a estrutura **ADRENTRY** original chamando a função [MAPIFreeBuffer](mapifreebuffer.md) e, em seguida, aloque a estrutura **ADRENTRY** de substituição com [ MAPIAllocateBuffer](mapiallocatebuffer.md).
  
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

