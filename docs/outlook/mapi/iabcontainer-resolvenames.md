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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405811"
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
  
> [in] Um ponteiro para uma [estrutura SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade que descrevem as propriedades a serem incluídas na estrutura [ADRLIST](adrlist.md) retornada pelo provedor. Para solicitar o conjunto padrão de propriedades do provedor, passe NULL no _parâmetro lpPropTagArray._ 
    
 _ulFlags_
  
> [in] Uma bitmask de sinalizadores que controla o tipo de texto nas cadeias de caracteres retornadas. Os sinalizadores a seguir podem ser definidos:
    
EMS_AB_ADDRESS_LOOKUP
  
> Somente as combinações exatas de endereço proxy serão encontradas; parciais são ignoradas. Esse sinalizador é suportado apenas pelo Provedor de Agenda do Exchange.
    
MAPI_CACHE_ONLY
  
> Somente o livro de endereços offline será usado para executar a resolução de nomes. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente abra a GAL (lista de endereços global) no modo cache do Exchange e acesse uma entrada nesse livro de endereços do cache sem criar tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas pelo Provedor de Agenda do Exchange. 
    
MAPI_UNICODE 
  
> As propriedades de cadeia de caracteres retornadas estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _lpAdrList_
  
> [in, out] Na entrada, um ponteiro para uma **estrutura ADRLIST** que contém a lista de destinatários a serem resolvidos. Na saída, um ponteiro para uma estrutura **ADRLIST** que contém os nomes resolvidos. 
    
 _lpFlagList_
  
> [in, out] Um ponteiro para uma matriz de sinalizadores, cada sinalizador correspondente a uma estrutura [ADRENTRY](adrentry.md) no parâmetro  _lpAdrList,_ que fornece o status da operação de resolução de nomes para o destinatário. Os sinalizadores no  _parâmetro lpFlagList_ estão na mesma ordem que as entradas em  _lpAdrList_. Os sinalizadores a seguir podem ser definidos:
    
MAPI_AMBIGUOUS 
  
> O destinatário correspondente foi resolvido, mas não para um identificador de entrada exclusivo. Outros contêineres não devem tentar resolver esse destinatário. 
    
MAPI_RESOLVED 
  
> O destinatário correspondente foi resolvido para um identificador de entrada exclusivo. Outros contêineres não devem tentar resolver esse destinatário. 
    
MAPI_UNRESOLVED 
  
> A entrada correspondente não foi resolvida. Outros contêineres devem tentar resolver esse destinatário.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O processo de resolução de nomes foi bem-sucedido.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação dá suporte apenas a Unicode.
    
MAPI_E_NO_SUPPORT 
  
> O provedor de agendas não dá suporte à resolução de nomes em massa usando esse método.
    
## <a name="remarks"></a>Comentários

O **método ResolveNames** tenta fazer a combinação de destinatários não resolvidos da matriz de entradas no parâmetro  _lpAdrList_ para destinatários neste contêiner de livro de endereços. Um destinatário não resolvido normalmente tem apenas a PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) e, possivelmente, algumas outras propriedades. Um destinatário não resolvido não tem a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), e seu sinalizador correspondente no parâmetro  _lpFlagList_ é definido como MAPI_UNRESOLVED. Por outro lado, um destinatário resolvido sempre tem pelo menos a propriedade **PR_ENTRYID,** além de várias outras propriedades, como **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)), **PR_DISPLAY_NAME** e **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)).
  
A resolução de nomes normalmente começa quando um cliente chama o [método IAddrBook::ResolveName.](iaddrbook-resolvename.md) O MAPI do Outlook responde chamando o método **ResolveNames** de cada contêiner de livro de endereços incluído no caminho de pesquisa do livro de endereços, especificado pela propriedade **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)). As entradas no parâmetro  _lpAdrList_ incluem destinatários já resolvidos porque estão em contêineres para os quais o MAPI já chamou **ResolveNames**, porque as entradas aparecem anteriormente no caminho de pesquisa. 
  
Cada contêiner tenta resolver as entradas não resolvidas, combinando o nome de exibição do destinatário com o nome de exibição de uma de suas entradas. Quando uma combinação exclusiva é encontrada, **ResolveNames** adiciona a propriedade **PR_ENTRYID** e outras propriedades incluídas no parâmetro  _lpPropTagArray_ à entrada correspondente na estrutura **ADRLIST** de saída. **ResolveNames** define a entrada no parâmetro  _lpFlagList_ como MAPI_RESOLVED. O identificador de entrada armazenado **na PR_ENTRYID** propriedade pode ser de curto ou longo prazo. 
  
Depois que todos os contêineres no caminho de pesquisa tentarem o processo de resolução de nomes, o MAPI abrirá uma caixa de diálogo, se possível, para solicitar ao usuário ajuda na resolução de conflitos restantes. 
  
Os clientes também podem usar a estrutura **ADRLIST retornada** em chamadas para o [método IMessage::ModifyRecipients.](imessage-modifyrecipients.md) 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Não é necessário dar suporte à resolução de nomes com o **método ResolveNames.** Em vez disso, ou adicionalmente, você pode dar suporte a ele com a **restrição de propriedade PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)). Se você decidir depender da restrição de **PR_ANR** para resolução de nomes, poderá retornar MAPI_E_NO_SUPPORT. Para obter mais informações, consulte [Implementando a resolução de nomes.](implementing-name-resolution.md)
  
Defina a entrada de sinalizador de um destinatário no parâmetro  _lpFlagList_ como MAPI_UNRESOLVED se o destinatário não corresponder a nenhum dos destinatários do contêiner. 
  
Quando um destinatário corresponde a vários destinatários, de definir seu sinalizador como MAPI_AMBIGUOUS e não alterar sua estrutura **ADRENTRY.** 
  
MAPI requires certain properties for recipients that are included in a message's recipient list. Você pode incluí-los na estrutura **ADRENTRY** como parte do processo de resolução de nomes ou aguardar que o MAPI solicite-os com chamadas para os métodos [IAddrBook::P repareRecips](iaddrbook-preparerecips.md) e [IMAPISupport::ExpandRecips.](imapisupport-expandrecips.md) Você pode eliminar essas chamadas extras e melhorar o desempenho incluindo as seguintes propriedades nas estruturas **ADRENTRY** de todos os destinatários resolvidos: 
  
- **PR_ADDRTYPE**
    
- **PR_DISPLAY_NAME**
    
- **PR_EMAIL_ADDRESS**
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
Se algumas das propriedades no parâmetro  _lpPropTagArray_ não estão disponíveis— normalmente porque a entrada do contêiner não dá suporte às propriedades e elas não estão incluídas no membro **ADRENTRY** do destinatário na estrutura **ADRLIST** — defina o tipo de propriedade de cada propriedade indisponível como PT_ERROR. 
  
Não remova nenhuma propriedade da estrutura **ADRENTRY** de um destinatário resolvido. 
  
Se você deve substituir em vez de modificar uma estrutura **ADRENTRY,** livre a estrutura **ADRENTRY** original primeiro chamando a função [MAPIFreeBuffer](mapifreebuffer.md) e, em seguida, aloque a estrutura **de substituição ADRENTRY** com [MAPIAllocateBuffer](mapiallocatebuffer.md).
  
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

