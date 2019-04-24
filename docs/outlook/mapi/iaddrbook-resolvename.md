---
title: IAddrBookResolveName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.ResolveName
api_type:
- COM
ms.assetid: a7823c16-efda-45c2-b931-3e1fbc823b0b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8a6a73153b857078cb37d94a634a6b0215a0a8c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287004"
---
# <a name="iaddrbookresolvename"></a>IAddrBook::ResolveName

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Realiza a resolução de nomes, atribuindo identificadores de entrada a destinatários em uma lista de destinatários.
  
```cpp
HRESULT ResolveName(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszNewEntryTitle,
  LPADRLIST lpAdrList
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> no Uma alça para a janela pai de uma caixa de diálogo exibida, se especificada, para solicitar que o usuário resolva a ambigüidade.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controlam vários aspectos do processo de resolução. Os seguintes sinalizadores podem ser definidos:
    
AB_UNICODEUI
  
> Indica que _lpszNewEntryTitle_ é uma cadeia de caracteres Unicode. 
    
MAPI_CACHE_ONLY
  
> Use apenas o catálogo de endereços offline para executar a resolução de nomes. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente Abra a lista de endereços global (GAL) no modo cache do Exchange e acesse uma entrada desse catálogo de endereços do cache sem criar tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.
    
MAPI_DIALOG 
  
> Exibe uma caixa de diálogo para solicitar ao usuário informações de resolução de nome adicionais. Se esse sinalizador não for definido, nenhuma caixa de diálogo será exibida. 
    
MAPI_UNICODE 
  
> Indica que as propriedades retornadas na lista de endereços devem ser do tipo PT_UNICODE em vez de PT_STRING8. 
    
 _lpszNewEntryTitle_
  
> no Um ponteiro para o texto do título do controle na caixa de diálogo que solicita que o usuário insira um destinatário. O título varia dependendo do tipo de destinatário. O parâmetro _lpszNewEntryTitle_ pode ser NULL. 
    
 _lpAdrList_
  
> [in-out] Um ponteiro para uma estrutura [das ADRLIST](adrlist.md) que contém a lista de nomes de destinatários a serem resolvidos. Essa estrutura **das ADRLIST** pode ser criada pelo método [IAddrBook:: address](iaddrbook-address.md) . 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O processo de resolução de nomes foi bem-sucedido.
    
MAPI_E_AMBIGUOUS_RECIP 
  
> Pelo menos um destinatário no parâmetro _lpAdrList_ corresponde a mais de uma entrada no catálogo de endereços. Normalmente, esse valor é retornado quando o sinalizador MAPI_DIALOG é definido, proibindo a exibição de uma caixa de diálogo. 
    
MAPI_E_NOT_FOUND 
  
> Pelo menos um destinatário no parâmetro _lpAdrList_ não pode ser resolvido. Normalmente, esse valor é retornado quando o sinalizador MAPI_DIALOG é definido, proibindo a exibição de uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

Os clientes e os provedores de **** serviços chamam o método ResolveName para iniciar o processo de resolução de nomes. Uma entrada não resolvida é uma entrada que ainda não tem um identificador de entrada ou uma propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
 **** O resolvedor passa pelo processo a seguir para cada entrada não resolvida na lista de endereços passada no parâmetro _lpAdrList_ . 
  
1. Se o tipo de endereço do destinatário aderir ao formato de um endereço SMTP (domínio _DisplayName_@ _. Top-Level-Domain_), ResolveName **** atribui um identificador de entrada one-off. 
    
2. Para cada contêiner na propriedade **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)), **ResolveName** chama o método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) . **ResolveNames** tenta corresponder o nome de exibição de cada destinatário não resolvido com um nome de exibição que pertença a uma de suas entradas. 
    
3. Se um contêiner não oferecer suporte **** a ResolveNames, **ResolveName** restringirá a tabela de conteúdo do contêiner usando uma restrição de propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)). Essa restrição faz com que o contêiner realize um tipo de "melhor palpite" de pesquisa para localizar um destinatário correspondente. Todos os contêineres devem oferecer suporte à restrição de propriedade **PR_ANR** . 
    
4. Quando um contêiner retorna um destinatário que corresponde a vários nomes **** , ResolveName exibe uma caixa de diálogo se o sinalizador MAPI_DIALOG estiver definido, o que permite ao usuário selecionar o nome correto. 
    
5. Se todos os contêineres da propriedade **PR_AB_SEARCH_PATH** tiverem sido chamados e se nenhuma correspondência for encontrada, o destinatário permanecerá não resolvido. 
    
Se um ou mais destinatários não forem resolvidos, **ResolveName** retornará MAPI_E_NOT_FOUND. Se um ou mais destinatários tinham uma resolução ambígua que não pôde ser resolvida com uma caixa de diálogo ou porque o sinalizador MAPI_DIALOG não foi **** definido, ResolveName retorna MAPI_E_AMBIGUOUS_RECIP. Quando alguns dos destinatários são ambíguos e alguns não podem ser resolvidos, **ResolveName** pode retornar um valor de erro. 
  
Se não for possível resolver um nome, o cliente poderá criar um endereço de one-off que tenha um endereço e um identificador de entrada especialmente formatados. Para obter mais informações sobre o formato de identificadores de entrada únicos, consulte [identificadores de entrada one-off](one-off-entry-identifiers.md). Para obter mais informações sobre o formato de endereços únicos, consulte [endereços one-off](one-off-addresses.md).
  
O MAPI oferece suporte a cadeias de caracteres Unicode para o **das ADRLIST** e os novos parâmetros de título de entrada para **resolver**; Se você definir o sinalizador MAPI_UNICODE, as seguintes propriedades serão retornadas como tipo PT_UNICODE nas estruturas [ADRENTRY](adrentry.md) : 
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
No enTanto, a propriedade **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) é sempre retornada como tipo PT_STRING8.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIABFunctions. cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI usa o **** método ResolveName para resolver um endereço one-off antes de adicioná-lo a uma mensagem.  <br/> |
|MAPIABFunctions. cpp  <br/> |AddRecipient  <br/> |MFCMAPI usa o **** método ResolveName para procurar uma entrada do catálogo de endereços por nome de exibição.  <br/> |
   
## <a name="see-also"></a>Confira também



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

