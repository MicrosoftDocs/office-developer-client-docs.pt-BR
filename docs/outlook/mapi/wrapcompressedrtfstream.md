---
title: WrapCompressedRTFStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.WrapCompressedRTFStream
api_type:
- COM
ms.assetid: 0949e066-aa28-4ede-ac88-b2dccd5098e8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a7095907a1fb437e225922d0bef08b4ad79a4b6f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594590"
---
# <a name="wrapcompressedrtfstream"></a>WrapCompressedRTFStream

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um fluxo de texto em descompactado Rich Text Format (RTF) do formato compactado usado na propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a>Parâmetros

 _lpCompressedRTFStream_
  
> [in] Ponteiro para um fluxo aberto na propriedade PR_RTF_COMPRESSED de uma mensagem. 
    
 _ulFlags_
  
> [in] Bitmask dos sinalizadores de opção para a função. Sinalizadores a seguir podem ser definidos:
    
MAPI_MODIFY 
  
> Se o cliente pretende ler ou gravar a interface de fluxo ajustado que será retornada. 
    
STORE_UNCOMPRESSED_RTF 
  
> RTF descompactado deve ser gravada no fluxo apontado pela _lpCompressedRTFStream_
    
 _lpUncompressedRTFStream_
  
> [out] Ponteiro para o local onde **WrapCompressedRTFStream** retorna um fluxo para o RTF descompactado. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Se o sinalizador MAPI_MODIFY é passado no parâmetro _ulFlags_ , o parâmetro _lpCompressedRTFStream_ já deve estar aberto para leitura e gravação. Novo e descompactado RTF texto deve ser gravado na interface da stream retornado em _lpUncompressedRTFStream_. Porque não é possível acrescentar stream existente, o texto da mensagem inteira deve ser gravado. 
  
Se o parâmetro _ulFlags_ é passado zero, então _lpCompressedRTFStream_ pode ser aberto somente leitura. Somente o texto da mensagem inteira pode ser lido para fora da interface do stream retornada em _lpUncompressedRTFStream_. Não é possível pesquisar iniciando ao meio do fluxo. 
  
 **WrapCompressedRTFStream** pressupõe que o ponteiro do fluxo compactado está definido como o início do stream. Determinados métodos OLE **IStream** não são suportados pelo fluxo descompactado retornado. Eles incluem **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat**e **IStream::UnlockRegion**. Para copiar para o fluxo inteiro, será necessária a um loop de leitura/gravação. 
  
Porque o cliente grava novo RTF no formato descompactado, ele deve usar **WrapCompressedRTFStream**, em vez de escrever diretamente no fluxo. Clientes RTF reconhecimento devem procurar o sinalizador STORE_UNCOMPRESSED_RTF na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) e passá-la para **WrapCompressed RTFStream** , se ela estiver definida. 
  
## <a name="see-also"></a>Confira também



[RTFSync](rtfsync.md)

