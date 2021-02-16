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
  
Chamado por um provedor de transporte para iniciar uma sessão TNEF (Formato de Encapsulamento Neutro) de Transporte MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Tnef.h  <br/> |
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
  
> [in] Passa um objeto de suporte ou passa NULL. 
    
_lpStream_
  
> [in] Ponteiro para uma interface OLE **IStream** do objeto de fluxo de armazenamento fornecendo uma origem ou destino para uma mensagem de fluxo TNEF. 
    
_lpszStreamName_
  
> [in] Ponteiro para o nome do fluxo de dados que o objeto TNEF usa. Se o chamador tiver definido o sinalizador TNEF_ENCODE ( _parâmetro ulFlags)_ em sua chamada para **OpenTnefStream**, o parâmetro  _lpszName_ deverá especificar um ponteiro não nulo para uma cadeia de caracteres não nula consistindo em quaisquer caracteres considerados válidos para nomear um arquivo. MAPI does not allow string names including the characters "[", "]" or ":", even if the file system permits their use. O tamanho da cadeia de caracteres passada para  _lpszName_ não deve exceder o valor de MAX_PATH, o comprimento máximo de uma cadeia de caracteres que contém um nome de caminho. 
    
_ulFlags_
  
> [in] Bitmask de sinalizadores usados para indicar o modo da função. Os sinalizadores a seguir podem ser definidos:
    
TNEF_BEST_DATA 
  
> Todas as propriedades possíveis são mapeadas para seus atributos de nível inferior, mas quando há uma possível perda de dados devido à conversão para um atributo de nível inferior, a propriedade também é codificada nos encapsulamentos. Observe que isso causará a duplicação de informações no fluxo TNEF. TNEF_BEST_DATA padrão se nenhum outro modo for especificado. 
    
TNEF_COMPATIBILITY 
  
> Fornece compatibilidade com versões mais antigas dos aplicativos cliente. Fluxos TNEF codificados com esse sinalizador mapearão todas as propriedades possíveis para seu atributo de nível inferior correspondente. Esse modo também faz com que o padrão de algumas propriedades que são exigidas por clientes de nível inferior. 
    
  > [!CAUTION]
  > Esse sinalizador está obsoleto e não deve ser usado. 
  
TNEF_DECODE 
  
> O objeto TNEF no fluxo indicado é aberto com acesso somente leitura. O provedor de transporte deve definir esse sinalizador se quiser que a função inicialize o objeto para decodificação subsequente.
    
TNEF_ENCODE 
  
> O objeto TNEF no fluxo indicado é aberto para permissão de leitura/gravação. O provedor de transporte deve definir esse sinalizador se quiser que a função inicialize o objeto para codificação subsequente.
    
TNEF_PURE 
  
> Codifica todas as propriedades nos blocos de encapsulamento MAPI. Portanto, um arquivo TNEF "puro" consistirá, no máximo, em attMAPIProps, attAttachment, attRenddata e attRecipTable. Esse modo é ideal para uso quando nenhuma compatibilidade com compatibilidade com trás é necessária.
    
_lpMessage_
  
> [in] Ponteiro para um objeto de mensagem como um destino para uma mensagem decodificada com anexos ou uma fonte para uma mensagem codificada com anexos. Qualquer propriedade de uma mensagem de destino pode ser substituída pelas propriedades de uma mensagem codificada.
    
_wKey_
  
> [in] Uma chave de pesquisa que o objeto TNEF usa para corresponder anexos às marcas de texto inseridas no texto da mensagem. Esse valor deve ser relativamente exclusivo entre mensagens.
    
_lppTNEF_
  
> [out] Ponteiro para o novo objeto TNEF.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Um objeto TNEF criado pela função **OpenTnefStream** chama posteriormente o método OLE **IUnknown::AddRef** para adicionar referências para o objeto de suporte, o objeto de fluxo e o objeto de mensagem. O provedor de transporte pode liberar as referências para todos os três objetos com uma única chamada para o método **OLE IUnknown::Release** no objeto TNEF. 
  
**OpenTnefStream** aloca e inicializa uma interface **ITnef** de objeto TNEF para o provedor usar na codificação de uma interface **IMessage** de mensagem MAPI em uma mensagem de fluxo TNEF. Como alternativa, a função pode configurar o objeto para o provedor usar em chamadas subsequentes para [ITnef::ExtractProps](itnef-extractprops.md) para decodificar uma mensagem de fluxo TNEF em uma mensagem MAPI. Para liberar o objeto TNEF e fechar a sessão, o provedor de transporte deve chamar o método **IUnknown::Release** herdado no objeto. 
  
Esta função é o ponto de entrada original para acesso TNEF e foi substituída por [OpenTnefStreamEx,](opentnefstreamex.md) mas ainda é usada para compatibilidade para aqueles que já usam TNEF. 
  
## <a name="see-also"></a>Confira também

- [IMAPISupport: IUnknown](imapisupportiunknown.md)
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md)

