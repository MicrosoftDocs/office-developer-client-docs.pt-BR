---
title: OpenTnefStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStream
api_type:
- COM
ms.assetid: 912d7799-53ce-42a7-9fbd-f9a6a3a56047
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 524b52026010b9a06d5822b48b7c04bbf90a113e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423955"
---
# <a name="opentnefstream"></a>OpenTnefStream

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Chamado por um provedor de transporte para iniciar uma sessão do formato de encapsulamento de transporte neutro (TNEF) MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |TNEF. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de transporte  <br/> |
   
```cpp
HRESULT OpenTnefStream(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName, 
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKey,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a>Parâmetros

_lpvSupport_
  
> no Passa um objeto support ou passa NULL. 
    
_lpStream_
  
> no Ponteiro para um objeto de fluxo de armazenamento interface **IStream** OLE que fornece uma origem ou um destino para uma mensagem de fluxo TNEF. 
    
_lpszStreamName_
  
> no Ponteiro para o nome do fluxo de dados que o objeto TNEF usa. Se o chamador tiver definido o sinalizador TNEF_ENCODE (parâmetro _parâmetroulflags_ ) em sua chamada para **OpenTnefStream**, o parâmetro _lpszName_ deverá especificar um ponteiro não nulo para uma cadeia de caracteres não nula que consista em qualquer caractere considerado válido para nomear um arquivo. O MAPI não permite nomes de cadeia de caracteres, incluindo os caracteres "[", "]" ou ":", mesmo se o sistema de arquivos permitir seu uso. O tamanho da cadeia de caracteres passada para _lpszName_ não deve exceder o valor de MAX_PATH, o tamanho máximo de uma cadeia de caracteres que contém um nome de caminho. 
    
_ulFlags_
  
> no Bitmask dos sinalizadores usados para indicar o modo da função. Os seguintes sinalizadores podem ser definidos:
    
TNEF_BEST_DATA 
  
> Todas as propriedades possíveis são mapeadas em seus atributos de nível inferior, mas quando há uma possível perda de dados devido à conversão em um atributo de nível inferior, a propriedade também é codificada nos encapsulamentos. Observe que isso causará a duplicação de informações no fluxo TNEF. TNEF_BEST_DATA é o padrão se nenhum outro modo for especificado. 
    
TNEF_COMPATIBILITY 
  
> Fornece compatibilidade com versões anteriores dos aplicativos cliente. Os fluxos TNEF codificados com esse sinalizador mapearão todas as propriedades possíveis para o atributo de nível inferior correspondente. Esse modo também faz com que o padrão de algumas propriedades exigidas por clientes de nível inferior. 
    
  > [!CAUTION]
  > Este sinalizador é obsoleto e não deve ser usado. 
  
TNEF_DECODE 
  
> O objeto TNEF no fluxo indicado é aberto com acesso somente leitura. O provedor de transporte deve definir esse sinalizador se quiser que a função inicialize o objeto para decodificação subsequente.
    
TNEF_ENCODE 
  
> O objeto TNEF no fluxo indicado é aberto para permissão de leitura/gravação. O provedor de transporte deve definir esse sinalizador se quiser que a função inicialize o objeto para a codificação subsequente.
    
TNEF_PURE 
  
> Codifica todas as propriedades nos blocos de encapsulamento MAPI. Portanto, um arquivo TNEF "puro" será composto de, no máximo, attMAPIProps, attAttachment, attRenddata e attRecipTable. Esse modo é ideal para uso quando não é necessária nenhuma compatibilidade com versões anteriores.
    
_lpMessage_
  
> no Ponteiro para um objeto Message como um destino para uma mensagem decodificada com anexos ou uma fonte para uma mensagem codificada com anexos. Todas as propriedades de uma mensagem de destino podem ser sobrescritas pelas propriedades de uma mensagem codificada.
    
_wKey_
  
> no Uma chave de pesquisa que o objeto TNEF usa para corresponder anexos às marcas de texto inseridas no texto da mensagem. Esse valor deve ser relativamente exclusivo nas mensagens.
    
_lppTNEF_
  
> bota Ponteiro para o novo objeto TNEF.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Um objeto TNEF criado pela função **OpenTnefStream** , posteriormente, chama o método OLE **IUnknown: AddRef** para adicionar referências para o objeto support, o objeto Stream e o objeto Message. O provedor de transporte pode liberar as referências para todos os três objetos com uma única chamada para o método OLE **IUnknown:: Release** no objeto TNEF. 
  
**OpenTnefStream** aloca e Inicializa uma interface de objeto **ITnef** do TNEF para o provedor usar na codificação de uma interface de **IMessage** de mensagem MAPI em uma mensagem de fluxo TNEF. Como alternativa, a função pode configurar o objeto para o provedor usar em chamadas subsequentes para [ITnef:: ExtractProps](itnef-extractprops.md) para decodificar uma mensagem de fluxo TNEF em uma mensagem MAPI. Para liberar o objeto TNEF e fechar a sessão, o provedor de transporte deve chamar o método **IUnknown:: Release** herdado no objeto. 
  
Esta função é o ponto de entrada original para acesso TNEF e foi substituído pelo [OpenTnefStreamEx](opentnefstreamex.md) , mas ainda é usado para compatibilidade com aqueles que já usam TNEF. 
  
## <a name="see-also"></a>Confira também

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)

