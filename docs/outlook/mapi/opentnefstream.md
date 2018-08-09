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
ms.openlocfilehash: 866d3be5e1c7a4375db84d1f15802e01f8d10f23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768188"
---
# <a name="opentnefstream"></a>OpenTnefStream

**Aplica-se a**: Outlook 
  
Chamado por um provedor de transporte para iniciar uma sessão MAPI TNEF Transport Neutral Encapsulation Format (). 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |TNEF.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de transporte  <br/> |
   
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
  
> [in] Passa um objeto de suporte ou passa em nulo. 
    
_lpStream_
  
> [in] Ponteiro para uma interface de OLE **IStream** do armazenamento stream objeto fornecimento de origem ou destino para uma mensagem de fluxo TNEF. 
    
_lpszStreamName_
  
> [in] Ponteiro para o nome do fluxo de dados que usa o objeto TNEF. Se o chamador tiver configurado o sinalizador TNEF_ENCODE (parâmetro _ulFlags_ ) na sua chamada **OpenTnefStream**, o parâmetro _lpszName_ deve especificar um ponteiro de não-nulo para uma cadeia de caracteres não-nulos consistindo quaisquer caracteres considerados válidos para nomear um arquivo. MAPI não permite nomes de cadeia de caracteres, incluindo os caracteres "[", "]", ou ":", mesmo se o seu uso permite que o sistema de arquivos. O tamanho da cadeia de caracteres passada para _lpszName_ não deve exceder o valor da MAX_PATH, o comprimento máximo de uma cadeia de caracteres que contém um nome de caminho. 
    
_ulFlags_
  
> [in] Bitmask dos sinalizadores usados para indicar o modo da função. Sinalizadores a seguir podem ser definidos:
    
TNEF_BEST_DATA 
  
> Todas as propriedades possíveis são mapeadas em seus atributos de baixo nível, mas, quando há uma possível perda de dados devido à conversão para um atributo de baixo nível, a propriedade também é codificada nos encapsulamentos. Observe que isso fará com que a duplicação de informações no stream TNEF. TNEF_BEST_DATA é o padrão se nenhum outros meios forem especificados. 
    
TNEF_COMPATIBILITY 
  
> Fornece os aplicativos de compatibilidade com versões anteriores com o cliente mais antigo. Fluxos TNEF codificados com esse sinalizador mapeará todas as propriedades possíveis em seu atributo de baixo nível correspondente. Este modo também fará com que o padrão é de algumas propriedades que são exigidas por clientes de nível inferior. 
    
  > [!CAUTION]
  > Esse sinalizador é obsoleto e não deve ser usado. 
  
TNEF_DECODE 
  
> O objeto TNEF no fluxo indicado é aberto com acesso somente leitura. O provedor de transporte deve definir esse sinalizador se desejar que a função para inicializar o objeto de decodificação subsequentes.
    
TNEF_ENCODE 
  
> O objeto TNEF no fluxo indicado é aberto para permissão de leitura/gravação. O provedor de transporte deve definir esse sinalizador se desejar que a função para inicializar o objeto para a codificação subsequentes.
    
TNEF_PURE 
  
> Codifica todas as propriedades nos blocos de encapsulamento de MAPI. Portanto, um arquivo TNEF "puro" consistirá em, no máximo, attMAPIProps, attAttachment, attRenddata e attRecipTable. Esse modo é ideal para uso quando sem compatibilidade com versões anteriores é necessária.
    
_lpMessage_
  
> [in] Ponteiro para um objeto de mensagem como um destino para uma mensagem decodificada com anexos ou em uma fonte de mensagem codificada com anexos. Todas as propriedades de uma mensagem de destino podem ser sobrescritas pelas propriedades de uma mensagem codificada.
    
_wKey_
  
> [in] Uma chave de pesquisa que o objeto TNEF usa para corresponder os anexos para as marcas de texto inseridos no texto da mensagem. Este valor deve ser exclusivo relativamente nas mensagens.
    
_lppTNEF_
  
> [out] Ponteiro para o novo objeto TNEF.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Um objeto TNEF criado pela função **OpenTnefStream** posteriormente chama o método OLE **AddRef** adicionar referências para o objeto de suporte, o objeto stream e o objeto de mensagem. O provedor de transporte pode liberar as referências para todos os três objetos com uma única chamada ao método OLE **IUnknown:: Release** no objeto TNEF. 
  
**OpenTnefStream** aloca e inicializa uma interface de **ITnef** do objeto TNEF para o provedor a ser usado em uma interface de **IMessage** de mensagem MAPI de codificação em uma mensagem de fluxo TNEF. Como alternativa, a função pode configurar o objeto para o provedor a ser usado em chamadas subsequentes para [ITnef::ExtractProps](itnef-extractprops.md) para decodificar uma mensagem de fluxo TNEF em uma mensagem MAPI. Para liberar o objeto TNEF e fechar a sessão, o provedor de transporte deve chamar o método **IUnknown:: Release** herdado no objeto. 
  
Essa função é o ponto de entrada original para acesso TNEF e foi substituída pelo [OpenTnefStreamEx](opentnefstreamex.md) , mas ainda é usada para compatibilidade para aqueles já usando TNEF. 
  
## <a name="see-also"></a>Confira também

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)

