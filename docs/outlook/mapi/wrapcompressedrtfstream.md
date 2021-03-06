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
ms.openlocfilehash: 710e0e2fc334194e33c6d8ba1296e4c7b1938bc0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439797"
---
# <a name="wrapcompressedrtfstream"></a>WrapCompressedRTFStream

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um fluxo de texto em RTF (Formato Rich Text) não compactado a partir do formato compactado usado na **propriedade PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)). 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos do cliente  <br/> |
   
```cpp
HRESULT WrapCompressedRTFStream(
  LPSTREAM lpCompressedRTFStream,
  ULONG ulflags,
  LPSTREAM FAR * lpUncompressedRTFStream
);
```

## <a name="parameters"></a>Parâmetros

 _lpCompressedRTFStream_
  
> [in] Ponteiro para um fluxo aberto na PR_RTF_COMPRESSED propriedade de uma mensagem. 
    
 _ulFlags_
  
> [in] Bitmask de sinalizadores de opção para a função. Os sinalizadores a seguir podem ser definidos:
    
MAPI_MODIFY 
  
> Se o cliente pretende ler ou gravar a interface de fluxo envolvida que é retornada. 
    
STORE_UNCOMPRESSED_RTF 
  
> RTF não compactado deve ser gravado no fluxo apontado por  _lpCompressedRTFStream_
    
 _lpUncompressedRTFStream_
  
> [out] Ponteiro para o local onde **WrapCompressedRTFStream** retorna um fluxo para o RTF não compactado. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Se o MAPI_MODIFY sinalizador for passado no  _parâmetro ulFlags,_ o parâmetro  _lpCompressedRTFStream_ já deverá estar aberto para leitura e escrita. O texto RTF novo e descompactado deve ser gravado na interface de fluxo retornada em  _lpUncompressedRTFStream_. Como não é possível anexar o fluxo existente, todo o texto da mensagem deve ser gravado. 
  
Se zero for passado no  _parâmetro ulFlags,_  _lpCompressedRTFStream_ poderá ser aberto somente leitura. Somente o texto inteiro da mensagem pode ser lido fora da interface de fluxo retornada em  _lpUncompressedRTFStream_. Não é possível pesquisar começando pelo meio do fluxo. 
  
 **WrapCompressedRTFStream** assume que o ponteiro do fluxo compactado está definido para o início do fluxo. Determinados métodos **OLE IStream** não são suportados pelo fluxo descompactado retornado. Eles incluem **IStream::Clone**, **IStream::LockRegion**, **IStream::Revert**, **IStream::Seek**, **IStream::SetSize**, **IStream::Stat** e **IStream::UnlockRegion**. Para copiar para todo o fluxo, um loop de leitura/gravação é necessário. 
  
Como o cliente grava o novo RTF no formato descompactado, ele deve usar **WrapCompressedRTFStream**, em vez de escrever diretamente no fluxo. Clientes com conhecimento de RTF devem procurar o sinalizador STORE_UNCOMPRESSED_RTF na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) e passá-lo para **WrapCompressed RTFStream** se ele estiver definido. 
  
## <a name="see-also"></a>Confira também



[RTFSync](rtfsync.md)

