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

## <a name="parameters"></a>Parâmetros

 _lpszName_
  
> no Um ponteiro para o valor da propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) do destinatário. O parâmetro _lpszName_ pode ser NULL. 
    
 _lpszAdrType_
  
> no Um ponteiro para o tipo de endereço do destinatário, como FAX ou SMTP. O parâmetro _lpszAdrType_ não pode ser nulo. 
    
 _lpszAddress_
  
> no Um ponteiro para o endereço do destinatário. O parâmetro _lpszAddress_ não pode ser nulo. 
    
 _ulFlags_
  
> no Uma máscara de bits de sinalizadores que afeta o destinatário one-off. Os seguintes sinalizadores podem ser definidos:
    
MAPI_SEND_NO_RICH_INFO 
  
> O destinatário não pode lidar com o conteúdo de mensagens formatados. Se MAPI_SEND_NO_RICH_INFO for definido, MAPI definirá a propriedade **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) do destinatário como false. Se MAPI_SEND_NO_RICH_INFO não for definido, MAPI definirá essa propriedade como TRUE, a menos que o endereço de email do destinatário apontado por _lpszAddress_ seja interpretado como um endereço de Internet. Nesse caso, o MAPI define **PR_SEND_RICH_INFO** como false. 
    
MAPI_UNICODE 
  
> O nome de exibição, o tipo de endereço e o endereço estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, essas cadeias de caracteres estarão no formato ANSI.
    
 _lpcbEntryID_
  
> bota Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEntryID_ . 
    
 _lppEntryID_
  
> bota Um ponteiro para um ponteiro para o identificador de entrada para o destinatário one-off.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O identificador de entrada one-off foi criado com êxito.
    
## <a name="remarks"></a>Comentários

Os clientes chamam o método **CreateOneOff** para criar um identificador de entrada para um destinatário one-off, que não pertence a nenhum contêiner de qualquer um dos provedores de catálogo de endereços carregados no momento. Os destinatários únicos podem ter qualquer tipo de endereço que seja suportado por um dos provedores de catálogos de endereços ativos da sessão. 
  
Os destinatários únicos são normalmente criados com um modelo para o seu tipo de endereço específico. O provedor de catálogo de endereços que oferece suporte ao tipo de endereço fornece o modelo. Um usuário de um aplicativo cliente insere as informações relevantes no modelo.
  
O MAPI oferece suporte a cadeias de caracteres Unicode para o nome de exibição, tipo de endereço e parâmetros de endereço de **CreateOneOff**.
  
O sinalizador MAPI_SEND_NO_RICH_INFO controla se o texto formatado no formato Rich Text (RTF) é enviado junto com cada mensagem. O formato de encapsulamento neutro de transporte (TNEF) — um formato que é usado para transmitir texto formatado — é enviado pela maioria dos provedores de transporte, independentemente de como o destinatário define sua propriedade **PR_SEND_RICH_INFO** . Isso não é um problema para clientes de mensagens que trabalham com mensagens interpessoais. No enTanto, como o TNEF geralmente é usado para enviar propriedades personalizadas para classes de mensagens personalizadas, não o suporte para ela pode ser um problema para clientes baseados em formulário ou clientes que exigem propriedades MAPI personalizadas. Para obter mais informações, consulte [enviando mensagens com TNEF](sending-messages-with-tnef.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|Mapiabfunctions. cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI usa o método **CreateOneOff** para criar uma ID de entrada para um endereço que não é encontrado em nenhum catálogo de endereços.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

