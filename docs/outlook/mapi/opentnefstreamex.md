---
title: OpenTnefStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStreamEx
api_type:
- COM
ms.assetid: eb84c408-2d8b-453b-92f4-5fd8851b84ca
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b651a913855e99e2f26dfd99fb725cc332201932
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565183"
---
# <a name="opentnefstreamex"></a>OpenTnefStreamEx

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um objeto Transport-Neutral Encapsulation Format (TNEF) que pode ser usado para codificar ou decodificar um objeto de mensagem em um fluxo de dados TNEF para uso por transportes ou gateways e repositórios de mensagem. Este é o ponto de entrada para acesso TNEF. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |TNEF.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de transporte  <br/> |
   
```cpp
HRESULT OpenTnefStreamEx(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName,
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKeyVal,
  LPADDRESSBOOK lpAddressBook,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a>Parâmetros

_lpvSupport_
  
> [in] Passa um objeto de suporte ou passa em nulo. Se for NULL, o parâmetro _lpAddressBook_ deve ser não-nulos. 
    
_lpStream_
  
> [in] Ponteiro para um objeto stream de armazenamento, como uma interface **IStream** do OLE, fornecendo origem ou destino para uma mensagem de fluxo TNEF. 
    
_lpszStreamName_
  
> [in] Ponteiro para o nome do fluxo de dados que usa o objeto TNEF. Se o chamador tiver configurado o sinalizador TNEF_ENCODE (parâmetro _ulFlags_ ) na sua chamada **OpenTnefStream**, o parâmetro _lpszName_ deve especificar um ponteiro de não-nulo para uma cadeia de caracteres não-nulos consistindo quaisquer caracteres considerados válidos para nomear um arquivo. MAPI não permite nomes de cadeia de caracteres, incluindo os caracteres "[", "]", ou ":", mesmo se o seu uso permite que o sistema de arquivos. O tamanho da cadeia de caracteres passada para o parâmetro _lpszName_ não deve exceder o valor da MAX_PATH, o comprimento máximo de uma cadeia de caracteres que contém um nome de caminho. 
    
_ulFlags_
  
> [in] Bitmask dos sinalizadores usados para indicar o modo da função. Sinalizadores a seguir podem ser definidos:
    
TNEF_BEST_DATA 
  
> Todas as propriedades possíveis são mapeadas em seus atributos de baixo nível, mas, quando há uma possível perda de dados devido à conversão para um atributo de baixo nível, a propriedade também é codificada nos encapsulamentos. Observe que isso fará com que a duplicação de informações no stream TNEF. TNEF_BEST_DATA é o padrão se nenhum outros meios forem especificados. 
    
TNEF_COMPATIBILITY 
  
> Fornece a compatibilidade com versões anteriores com aplicativos mais antigos do cliente. Fluxos TNEF codificados com esse sinalizador mapeará todas as propriedades possíveis em seu atributo de baixo nível correspondente. Este modo também fará com que o padrão é de algumas propriedades que são exigidas por clientes de nível inferior. 
    
  > [!CAUTION]
  > Esse sinalizador é obsoleto e não deve ser usado. 
  
TNEF_DECODE 
  
> O objeto TNEF no fluxo indicado é aberto com acesso somente leitura. O provedor de transporte deve definir esse sinalizador se a função for inicializar o objeto de decodificação subsequentes.
    
TNEF_ENCODE 
  
> O objeto TNEF no fluxo indicado é aberto para permissão de leitura/gravação. O provedor de transporte deve definir esse sinalizador se a função for inicializar o objeto para a codificação subsequentes.
    
TNEF_PURE 
  
> Codifica todas as propriedades nos blocos de encapsulamento de MAPI. Portanto, um arquivo TNEF "puro" consistirá em, no máximo, os atributos attMAPIProps, attAttachment, attRenddata e attRecipTable. Esse modo é ideal para uso quando sem compatibilidade com versões anteriores é necessária.
    
_lpMessage_
  
> [in] Ponteiro para um objeto de mensagem como um destino para uma mensagem decodificada com anexos ou em uma fonte de mensagem codificada com anexos. Todas as propriedades de uma mensagem de destino podem ser substituídas pelas propriedades de uma mensagem codificada.
    
_wKeyVal_
  
> [in] Uma chave de pesquisa que o objeto TNEF usa para corresponder os anexos para as marcas de texto inseridos no texto da mensagem. Este valor deve ser exclusivo relativamente nas mensagens. 
    
_lpAddressBook_
  
> [in] Ponteiro para um objeto de catálogo de endereços usado para obter as informações de identificadores de entrada de endereçamento. 
    
_lppTNEF_
  
> [out] Ponteiro para o novo objeto TNEF.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

A função **OpenTnefStreamEx** é o substituto recomendado para [OpenTnefStream](opentnefstream.md), o ponto de entrada original para acesso TNEF. 
  
Um objeto TNEF criado pela função **OpenTnefStreamEx** posteriormente chama o método OLE **AddRef** adicionar referências para o objeto de suporte, o objeto stream e o objeto de mensagem. O provedor de transporte pode liberar as referências para todos os três objetos com uma única chamada ao método OLE **IUnknown:: Release** no objeto TNEF. 
  
**OpenTnefStreamEx** aloca e inicializa um objeto TNEF para o provedor a ser usado em uma mensagem MAPI de codificação em uma mensagem de fluxo TNEF. Como alternativa, essa função pode configurar o objeto para o provedor a ser usado em chamadas subsequentes para [ITnef::ExtractProps](itnef-extractprops.md) para decodificar uma mensagem de fluxo TNEF em uma mensagem MAPI. Para liberar o objeto TNEF e fechar a sessão, o provedor de transporte deve chamar o método **IUnknown:: Release** herdado no objeto. 
  
O valor de base para o parâmetro _wKeyVal_ não deve ser zero e não deve ser o mesmo para cada chamada para **OpenTnefStreamEx**. Em vez disso, use números aleatórios com base na hora do sistema do gerador de números aleatórios da biblioteca de tempo de execução.
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|CPP  <br/> |LoadFromTNEF  <br/> |MFCMAPI usa o método **OpenTnefStreamEx** para abrir um fluxo no arquivo TNEF, portanto, podem ser extraídas propriedades.  <br/> |
   
## <a name="see-also"></a>Confira também

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

