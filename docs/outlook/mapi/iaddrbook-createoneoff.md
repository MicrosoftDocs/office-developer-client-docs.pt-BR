---
title: IAddrBookCreateOneOff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.CreateOneOff
api_type:
- COM
ms.assetid: bcacfbdf-edff-4810-a985-e6d2c9271901
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: fefd81a7d6cdfda24df93ec928cd3305cb8ef8be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766867"
---
# <a name="iaddrbookcreateoneoff"></a>IAddrBook::CreateOneOff

  
  
**Aplica-se a**: Outlook 
  
Cria um identificador de entrada para um endereço one-off.
  
```cpp
HRESULT CreateOneOff(
  LPSTR lpszName,
  LPSTR lpszAdrType,
  LPSTR lpszAddress,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Par�metros

 _lpszName_
  
> [in] Um ponteiro para o valor da propriedade de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) do destinatário. O parâmetro _lpszName_ pode ser NULL. 
    
 _lpszAdrType_
  
> [in] Um ponteiro para o tipo de endereço do destinatário, como FAX ou SMTP. O parâmetro _lpszAdrType_ não pode ser NULL. 
    
 _lpszAddress_
  
> [in] Um ponteiro para o endereço do destinatário. O parâmetro _lpszAddress_ não pode ser NULL. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que afeta o destinatário único. Sinalizadores a seguir podem ser definidos:
    
MAPI_SEND_NO_RICH_INFO 
  
> O destinatário não pode manipular o conteúdo da mensagem formatada. Se MAPI_SEND_NO_RICH_INFO for definido, o MAPI define a propriedade de **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) do destinatário como FALSE. Se MAPI_SEND_NO_RICH_INFO não estiver definida, o MAPI define essa propriedade como TRUE, a menos que o endereço do destinatário mensagens apontado pela _lpszAddress_ é interpretado como um endereço de Internet. Nesse caso, MAPI define **PR_SEND_RICH_INFO** como FALSE. 
    
MAPI_UNICODE 
  
> O nome para exibição, tipo de endereço e endereço estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, essas cadeias de caracteres estão no formato ANSI.
    
 _lpcbEntryID_
  
> [out] Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Um ponteiro para um ponteiro para o identificador de entrada para o destinatário único.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O identificador de entrada únicos foi criado com êxito.
    
## <a name="remarks"></a>Coment�rios

Clientes chamar o método **CreateOneOff** para criar um identificador de entrada para um destinatário único — um destinatário que não pertençam a qualquer um dos contêineres de qualquer um dos provedores de catálogo de endereços atualmente carregado. Destinatários únicos podem ter qualquer tipo de endereço que é suportado por um dos provedores de catálogo de endereços ativo para a sessão. 
  
Destinatários únicos normalmente são criados com um modelo para seus tipos de endereço específica. O provedor de catálogo de endereços que suporta o tipo de endereço fornece o modelo. Um usuário de um aplicativo cliente inserir as informações relevantes para o modelo.
  
MAPI suporta as sequências de caracteres Unicode para o nome para exibição, tipo de endereço e os parâmetros de endereço de **CreateOneOff**.
  
O sinalizador MAPI_SEND_NO_RICH_INFO controla se o texto formatado no formato Rich Text (RTF) é enviado junto com cada mensagem. O TNEF Transport Neutral Encapsulation Format () — é usado para transmitir um formato de texto formatado — é enviada pelo maioria dos provedores de transporte, independentemente de como o destinatário define sua propriedade **PR_SEND_RICH_INFO** . Isso não é um problema para clientes que funcionam com interpessoais emails de mensagens. No entanto, porque o TNEF geralmente é utilizado para enviar propriedades personalizadas para classes de mensagem personalizada, não oferece suporte à pode ser um problema para clientes baseados no formulário ou clientes que requerem propriedades personalizadas de MAPI. Para obter mais informações, consulte [Envio de mensagens com TNEF](sending-messages-with-tnef.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|Mapiabfunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI usa o método **CreateOneOff** para criar uma identificação de entrada para um endereço que não for encontrado em qualquer catálogo de endereços.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)
  
[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

