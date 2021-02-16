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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408128"
---
# <a name="iaddrbookresolvename"></a>IAddrBook::ResolveName

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Executa a resolução de nomes, atribuindo identificadores de entrada a destinatários em uma lista de destinatários.
  
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
  
> [in] Um alça para a janela pai de uma caixa de diálogo que é mostrada, se especificada, para solicitar que o usuário resolva a ambiguidade.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controlam vários aspectos do processo de resolução. Os sinalizadores a seguir podem ser definidos:
    
AB_UNICODEUI
  
> Indica que  _lpszNewEntryTitle_ é uma cadeia de caracteres UNICODE. 
    
MAPI_CACHE_ONLY
  
> Use somente o livro de endereços offline para executar a resolução de nomes. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente abra a GAL (lista de endereços global) no modo cache do Exchange e acesse uma entrada nesse livro de endereços do cache sem criar tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas pelo Provedor de Agenda do Exchange.
    
MAPI_DIALOG 
  
> Exibe uma caixa de diálogo para solicitar ao usuário informações adicionais de resolução de nomes. Se esse sinalizador não estiver definido, nenhuma caixa de diálogo será exibida. 
    
MAPI_UNICODE 
  
> Indica que as propriedades retornadas na lista de endereços devem ser do tipo PT_UNICODE em vez de PT_STRING8. 
    
 _lpszNewEntryTitle_
  
> [in] Um ponteiro para o texto do título do controle na caixa de diálogo que solicita que o usuário insira um destinatário. O título varia dependendo do tipo de destinatário. O  _parâmetro lpszNewEntryTitle_ pode ser NULL. 
    
 _lpAdrList_
  
> [in-out] Um ponteiro para uma [estrutura ADRLIST](adrlist.md) que contém a lista de nomes de destinatários a serem resolvidos. Essa **estrutura ADRLIST** pode ser criada pelo [método IAddrBook::Address.](iaddrbook-address.md) 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O processo de resolução de nomes foi bem-sucedido.
    
MAPI_E_AMBIGUOUS_RECIP 
  
> Pelo menos um destinatário no parâmetro  _lpAdrList_ corresponderam a mais de uma entrada no livro de endereços. Normalmente, esse valor é retornado quando o sinalizador MAPI_DIALOG é definido, proibindo a exibição de uma caixa de diálogo. 
    
MAPI_E_NOT_FOUND 
  
> Pelo menos um destinatário no parâmetro  _lpAdrList_ não pode ser resolvido. Normalmente, esse valor é retornado quando o sinalizador MAPI_DIALOG é definido, proibindo a exibição de uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

Os clientes e provedores de serviços chamam o **método ResolveName** para iniciar o processo de resolução de nomes. Uma entrada não resolvida é uma entrada que ainda não tem um identificador de entrada **ou** uma PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
 **ResolveName** passa pelo processo a seguir para cada entrada não resolvida na lista de endereços passada no _parâmetro lpAdrList._ 
  
1. Se o tipo de endereço do destinatário aderir ao formato de um endereço SMTP ( _displayname_ @  _domain.top-level-domain_), **ResolveName** atribuirá a ele um identificador de entrada único. 
    
2. Para cada contêiner na **propriedade PR_AB_SEARCH_PATH** ([PidTagAbSearchPath](pidtagabsearchpath-canonical-property.md)), **ResolveName** chama o método [IABContainer::ResolveNames.](iabcontainer-resolvenames.md) **ResolveNames** tenta corresponder ao nome de exibição de cada destinatário não resolvido com um nome de exibição que pertence a uma de suas entradas. 
    
3. Se um contêiner não tiver suporte para **ResolveNames,** **ResolveName** restringirá a tabela de conteúdo do contêiner usando uma restrição de propriedade **PR_ANR** ([PidTagAnr).](pidtaganr-canonical-property.md) Essa restrição faz com que o contêiner execute um tipo de pesquisa de "melhor suposição" para localizar um destinatário correspondente. Todos os contêineres devem suportar a **restrição PR_ANR** propriedade. 
    
4. Quando um contêiner retorna um destinatário que corresponde a vários nomes, **ResolveName** exibe uma caixa de diálogo se o sinalizador MAPI_DIALOG estiver definido, o que permite que o usuário selecione o nome correto. 
    
5. Se todos os contêineres na propriedade **PR_AB_SEARCH_PATH** foram chamados e nenhuma combinação foi encontrada, o destinatário permanece não resolvido. 
    
Se um ou mais destinatários não tiverem resolvido, **ResolveName** retornará MAPI_E_NOT_FOUND. Se um ou mais destinatários tiveram resolução ambígua que não pôde ser resolvida com uma caixa de diálogo ou porque o sinalizador MAPI_DIALOG não foi definido, **ResolveName** retornará MAPI_E_AMBIGUOUS_RECIP. Quando alguns dos destinatários são ambíguos e outros não podem ser resolvidos, **ResolveName** pode retornar qualquer um dos valores de erro. 
  
Se um nome não puder ser resolvido, o cliente poderá criar um endereço único que tenha um endereço especialmente formatado e um identificador de entrada. Para obter mais informações sobre o formato de identificadores de entrada único, consulte [Identificadores de entrada único.](one-off-entry-identifiers.md) Para obter mais informações sobre o formato de endereços one-off, consulte [Endereços One-Off.](one-off-addresses.md)
  
MAPI supports Unicode character strings for the **ADRLIST** and the new entry title parameters to **ResolveName**; se você definir o sinalizador MAPI_UNICODE, as seguintes propriedades serão retornadas como tipos PT_UNICODE estruturas [ADRENTRY:](adrentry.md) 
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
    
- **PR_TRANSMITABLE_DISPLAY_NAME** ([PidTagTransmittableDisplayName](pidtagtransmittabledisplayname-canonical-property.md))
    
No entanto, **a PR_7BIT_DISPLAY_NAME** ([PidTag7BitDisplayName](pidtag7bitdisplayname-canonical-property.md)) é sempre retornada como tipo PT_STRING8.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI usa o **método ResolveName** para resolver um endereço único antes de adiá-lo a uma mensagem.  <br/> |
|MAPIABFunctions.cpp  <br/> |AddRecipient  <br/> |MFCMAPI usa o **método ResolveName** para procurar uma entrada do livro de endereços por nome de exibição.  <br/> |
   
## <a name="see-also"></a>Confira também



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

