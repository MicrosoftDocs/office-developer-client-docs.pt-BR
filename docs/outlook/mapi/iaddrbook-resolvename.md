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
ms.openlocfilehash: aa72085c4e50fcef1f2d3da81e5409af3d55d89b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766868"
---
# <a name="iaddrbookresolvename"></a>IAddrBook::ResolveName

  
  
**Aplica-se a**: Outlook 
  
Executa a resolução de nomes, atribuindo identificadores de entrada para destinatários em uma lista de destinatários.
  
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
  
> [in] Um identificador para a janela pai de uma caixa de diálogo que é exibida, se especificado, para avisar o usuário resolva ambiguidade.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controlam os vários aspectos do processo de resolução. Sinalizadores a seguir podem ser definidos:
    
AB_UNICODEUI
  
> Indica que _lpszNewEntryTitle_ é uma cadeia de caracteres UNICODE. 
    
MAPI_CACHE_ONLY
  
> Use somente o catálogo de endereços offline para executar a resolução de nomes. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente para abrir a lista de endereços global (GAL) no modo cache do exchange e acessar uma entrada no catálogo de endereços do cache sem criar o tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.
    
MAPI_DIALOG 
  
> Exibe uma caixa de diálogo para solicitar ao usuário para obter informações de resolução de nome adicional. Se esse sinalizador não estiver definida, nenhuma caixa de diálogo é exibida. 
    
MAPI_UNICODE 
  
> Indica que as propriedades retornadas na lista de endereços devem ser do tipo PT_UNICODE em vez de PT_STRING8. 
    
 _lpszNewEntryTitle_
  
> [in] Um ponteiro para o texto do título do controle na caixa de diálogo que solicita ao usuário inserir um destinatário. O título varia dependendo do tipo de destinatário. O parâmetro _lpszNewEntryTitle_ pode ser NULL. 
    
 _lpAdrList_
  
> [em-out] Um ponteiro para uma estrutura [ADRLIST](adrlist.md) que contém a lista de nomes de destinatários para ser resolvido. Essa estrutura **ADRLIST** pode ser criada pelo método [IAddrBook::Address](iaddrbook-address.md) . 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O processo de resolução de nome bem-sucedido.
    
MAPI_E_AMBIGUOUS_RECIP 
  
> Pelo menos um destinatário no parâmetro _lpAdrList_ correspondente mais de uma entrada no catálogo de endereços. Geralmente, esse valor é retornado quando o sinalizador MAPI_DIALOG estiver definido, impedindo a exibição de uma caixa de diálogo. 
    
E_NOT_FOUND 
  
> Pelo menos um destinatário no parâmetro _lpAdrList_ não pode ser resolvido. Geralmente, esse valor é retornado quando o sinalizador MAPI_DIALOG estiver definido, impedindo a exibição de uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

Clientes e provedores de serviços de chamar o método de **ResolveName** para iniciar o processo de resolução de nome. Uma entrada não resolvida é uma entrada que ainda não tem um identificador de entrada ou a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
 **ResolveName** vai através do seguinte processo para cada entrada não resolvido na lista de endereços passada no parâmetro _lpAdrList_ . 
  
1. Se o tipo de endereço do destinatário de acordo com o formato de um endereço SMTP ( _displayname_@ _domain.top de nível de domínio_), **ResolveName** atribui um identificador de entrada únicos. 
    
2. Para cada contêiner na propriedade **PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)), **ResolveName** chama o método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) . **ResolveNames** tenta corresponder ao nome de exibição de cada destinatário não resolvido com um nome de exibição que pertence a uma das suas entradas. 
    
3. Se um contêiner não oferece suporte a **ResolveNames**, **ResolveName** restringe a tabela de conteúdo do contêiner usando uma restrição de propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)). Essa restrição faz com que o contêiner executar um tipo de "melhor adivinhar" de pesquisa para localizar um destinatário correspondente. Todos os contêineres devem oferecer suporte a restrição de propriedade **PR_ANR** . 
    
4. Quando um contêiner retorna um destinatário que corresponda a vários nomes, **ResolveName** exibe uma caixa de diálogo, se o sinalizador MAPI_DIALOG estiver definido, o que permite que o usuário selecione o nome correto. 
    
5. Se todos os contêineres na propriedade **PR_AB_SEARCH_PATH** tem sido chamados e nenhuma correspondência foi encontrada, o destinatário permanece não resolvido. 
    
Se um ou mais destinatários estão não resolvidos, **ResolveName** retorna E_NOT_FOUND. Se um ou mais destinatários tinham ambígua resolução que não puderam ser resolvida com uma caixa de diálogo ou porque o sinalizador MAPI_DIALOG não foi definido, **ResolveName** retorna MAPI_E_AMBIGUOUS_RECIP. Quando são alguns dos destinatários ambíguos e alguns não puderem ser solucionadas, **ResolveName** pode retornar qualquer valor de erro. 
  
Se um nome não pode ser resolvido, o cliente pode criar um endereço único que tenha um endereço especialmente formatado e o identificador de entrada. Para obter mais informações sobre o formato dos identificadores de entrada únicos, consulte [Identificadores de entrada únicos](one-off-entry-identifiers.md). Para obter mais informações sobre o formato dos endereços únicos, consulte [Endereços únicos](one-off-addresses.md).
  
MAPI oferece suporte a cadeias de caracteres Unicode para o **ADRLIST** e os novos parâmetros de título de entrada para **ResolveName**; Se você definir o sinalizador MAPI_UNICODE, as seguintes propriedades são retornadas como tipo PT_UNICODE nas estruturas [ADRENTRY](adrentry.md) : 
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
No entanto, a propriedade **PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) sempre será retornada enquanto digita PT_STRING8.
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI usa o método **ResolveName** para resolver um endereço único antes de adicioná-lo a uma mensagem.  <br/> |
|MAPIABFunctions.cpp  <br/> |AddRecipient  <br/> |MFCMAPI usa o método **ResolveName** para procurar uma entrada do catálogo de endereços por nome para exibição.  <br/> |
   
## <a name="see-also"></a>Confira também



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

