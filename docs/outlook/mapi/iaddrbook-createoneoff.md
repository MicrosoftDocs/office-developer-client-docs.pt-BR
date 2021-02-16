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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 980ac82c6f7fcb5771a6013b3fb033b0bdfd05e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427378"
---
# <a name="iaddrbookcreateoneoff"></a>IAddrBook::CreateOneOff

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um identificador de entrada para um endereço único.
  
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

## <a name="parameters"></a>Parâmetros

 _lpszName_
  
> [in] Um ponteiro para o valor da propriedade PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)) do destinatário. O  _parâmetro lpszName_ pode ser NULL. 
    
 _lpszAdrType_
  
> [in] Um ponteiro para o tipo de endereço do destinatário, como FAX ou SMTP. O  _parâmetro lpszAdrType_ não pode ser NULL. 
    
 _lpszAddress_
  
> [in] Um ponteiro para o endereço do destinatário. O  _parâmetro lpszAddress_ não pode ser NULL. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que afeta o destinatário único. Os sinalizadores a seguir podem ser definidos:
    
MAPI_SEND_NO_RICH_INFO 
  
> O destinatário não pode manipular o conteúdo da mensagem formatada. Se MAPI_SEND_NO_RICH_INFO for definida, MAPI definirá a propriedade **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) do destinatário como FALSE. Se MAPI_SEND_NO_RICH_INFO não estiver definido, o MAPI definirá essa propriedade como TRUE, a menos que o endereço de mensagens do destinatário apontado por  _lpszAddress_ seja interpretado como um endereço da Internet. Nesse caso, MAPI **define** PR_SEND_RICH_INFO como FALSE. 
    
MAPI_UNICODE 
  
> O nome de exibição, o tipo de endereço e o endereço estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, essas cadeias de caracteres estão no formato ANSI.
    
 _lpcbEntryID_
  
> [out] Um ponteiro para a contagem de byte no identificador de entrada apontado pelo _parâmetro lppEntryID._ 
    
 _lppEntryID_
  
> [out] Um ponteiro para um ponteiro para o identificador de entrada para o destinatário único.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O identificador de entrada único foi criado com êxito.
    
## <a name="remarks"></a>Comentários

Os clientes chamam o método **CreateOneOff** para criar um identificador de entrada para um destinatário único — um destinatário que não pertence a nenhum dos contêineres de qualquer um dos provedores de agendamento de endereços carregados no momento. Os destinatários one-off podem ter qualquer tipo de endereço suportado por um dos provedores de agendas ativos da sessão. 
  
Destinatários one-off geralmente são criados com um modelo para seu tipo de endereço específico. O provedor de agendas que oferece suporte ao tipo de endereço fornece o modelo. Um usuário de um aplicativo cliente ins informa as informações relevantes no modelo.
  
MAPI supports Unicode character strings for the display name, address type, and address parameters of **CreateOneOff**.
  
O MAPI_SEND_NO_RICH_INFO sinalizador controla se o texto formatado no formato Rich Text (RTF) é enviado junto com cada mensagem. O TNEF (Transport Neutral Encapsulation Format) — um formato usado para transmitir texto formatado — é enviado pela maioria dos provedores de transporte, independentemente de como o destinatário define sua propriedade **PR_SEND_RICH_INFO.** Isso não é um problema para clientes de mensagens que trabalham com mensagens interpersonales. No entanto, como o TNEF normalmente é usado para enviar propriedades personalizadas para classes de mensagens personalizadas, não oferecer suporte a ele pode ser um problema para clientes baseados em formulário ou clientes que exigem propriedades MAPI personalizadas. Para obter mais informações, consulte [Enviando mensagens com TNEF](sending-messages-with-tnef.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|Mapiabfunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI usa o **método CreateOneOff** para criar uma ID de entrada para um endereço que não é encontrado em nenhum livro de endereços.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

