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
ms.openlocfilehash: 178ab67875d8fb442500dd412dbafe4403deee16
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406238"
---
# <a name="opentnefstreamex"></a>OpenTnefStreamEx

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um objeto TNEF (Transport-neutral Encapsulation Format) que pode ser usado para codificar ou decodificar um objeto Message em um fluxo de dados TNEF para uso por transportes ou gateways e repositórios de mensagens. Este é o ponto de entrada para acesso TNEF. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |TNEF. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de transporte  <br/> |
   
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
  
> no Passa um objeto support ou passa NULL. Se NULL, o parâmetro _lpAddressBook_ deve ser não nulo. 
    
_lpStream_
  
> no Ponteiro para um objeto de fluxo de armazenamento, como uma interface de **IStream** OLE, fornecendo uma origem ou um destino para uma mensagem de fluxo TNEF. 
    
_lpszStreamName_
  
> no Ponteiro para o nome do fluxo de dados que o objeto TNEF usa. Se o chamador tiver definido o sinalizador TNEF_ENCODE (parâmetro _parâmetroulflags_ ) em sua chamada para **OpenTnefStream**, o parâmetro _lpszName_ deverá especificar um ponteiro não nulo para uma cadeia de caracteres não nula que consista em qualquer caractere considerado válido para nomear um arquivo. O MAPI não permite nomes de cadeia de caracteres, incluindo os caracteres "[", "]" ou ":", mesmo se o sistema de arquivos permitir seu uso. O tamanho da cadeia de caracteres passada para o parâmetro _lpszName_ não deve exceder o valor de MAX_PATH, o tamanho máximo de uma cadeia de caracteres que contém um nome de caminho. 
    
_ulFlags_
  
> no Bitmask dos sinalizadores usados para indicar o modo da função. Os seguintes sinalizadores podem ser definidos:
    
TNEF_BEST_DATA 
  
> Todas as propriedades possíveis são mapeadas em seus atributos de nível inferior, mas quando há uma possível perda de dados devido à conversão em um atributo de nível inferior, a propriedade também é codificada nos encapsulamentos. Observe que isso causará a duplicação de informações no fluxo TNEF. TNEF_BEST_DATA é o padrão se nenhum outro modo for especificado. 
    
TNEF_COMPATIBILITY 
  
> Fornece compatibilidade com aplicativos cliente mais antigos. Os fluxos TNEF codificados com esse sinalizador mapearão todas as propriedades possíveis para o atributo de nível inferior correspondente. Esse modo também faz com que o padrão de algumas propriedades exigidas por clientes de nível inferior. 
    
  > [!CAUTION]
  > Este sinalizador é obsoleto e não deve ser usado. 
  
TNEF_DECODE 
  
> O objeto TNEF no fluxo indicado é aberto com acesso somente leitura. O provedor de transporte deve definir esse sinalizador se a função for inicializar o objeto para decodificação subsequente.
    
TNEF_ENCODE 
  
> O objeto TNEF no fluxo indicado é aberto para permissão de leitura/gravação. O provedor de transporte deve definir esse sinalizador se a função for inicializar o objeto para a codificação subsequente.
    
TNEF_PURE 
  
> Codifica todas as propriedades nos blocos de encapsulamento MAPI. Portanto, um arquivo TNEF "puro" será composto de, no máximo, os atributos attMAPIProps, attAttachment, attRenddata e attRecipTable. Esse modo é ideal para uso quando não é necessária nenhuma compatibilidade com versões anteriores.
    
_lpMessage_
  
> no Ponteiro para um objeto Message como um destino para uma mensagem decodificada com anexos ou uma fonte para uma mensagem codificada com anexos. Todas as propriedades de uma mensagem de destino podem ser substituídas pelas propriedades de uma mensagem codificada.
    
_wKeyVal_
  
> no Uma chave de pesquisa que o objeto TNEF usa para corresponder anexos às marcas de texto inseridas no texto da mensagem. Esse valor deve ser relativamente exclusivo nas mensagens. 
    
_lpAddressBook_
  
> no Ponteiro para um objeto de catálogo de endereços usado para obter informações de endereçamento para identificadores de entrada. 
    
_lppTNEF_
  
> bota Ponteiro para o novo objeto TNEF.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

A função **OpenTnefStreamEx** é a substituição recomendada para o [OpenTnefStream](opentnefstream.md), o ponto de entrada original para acesso TNEF. 
  
Um objeto TNEF criado pela função **OpenTnefStreamEx** , posteriormente, chama o método OLE **IUnknown: AddRef** para adicionar referências para o objeto support, o objeto Stream e o objeto Message. O provedor de transporte pode liberar as referências para todos os três objetos com uma única chamada para o método OLE **IUnknown:: Release** no objeto TNEF. 
  
**OpenTnefStreamEx** aloca e inicializa um objeto TNEF para o provedor usar na codificação de uma mensagem MAPI em uma mensagem de fluxo TNEF. Como alternativa, essa função pode configurar o objeto para o provedor usar em chamadas subsequentes para [ITnef:: ExtractProps](itnef-extractprops.md) para decodificar uma mensagem de fluxo TNEF em uma mensagem MAPI. Para liberar o objeto TNEF e fechar a sessão, o provedor de transporte deve chamar o método **IUnknown:: Release** herdado no objeto. 
  
O valor base para o parâmetro _wKeyVal_ não deve ser zero e não deve ser o mesmo para todas as chamadas para **OpenTnefStreamEx**. Em vez disso, use números aleatórios com base na hora do sistema do gerador de números aleatórios da biblioteca de tempo de execução.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|Arquivo. cpp  <br/> |LoadFromTNEF  <br/> |MFCMAPI usa o método **OpenTnefStreamEx** para abrir um Stream no arquivo TNEF para que as propriedades possam ser extraídas.  <br/> |
   
## <a name="see-also"></a>Confira também

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
- [MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

