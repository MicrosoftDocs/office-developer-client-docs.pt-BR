---
title: ITnef IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef
api_type:
- COM
ms.assetid: eddca896-9497-4425-9904-87ef3cbae298
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: e8267b254648870cea4e16b4dea0e9c92e316fb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767750"
---
# <a name="itnef--iunknown"></a>ITnef: IUnknown

  
  
**Aplica-se a**: Outlook 
  
Fornece métodos para encapsular propriedades MAPI que não são suportadas por um sistema de mensagens em binários fluxos que podem ser anexados às mensagens. O formato usado para este encapsulamento é o transporte-TNEF Neutral Encapsulation Format (). O provedor de transporte de destino ou de um aplicativo cliente baseado em MAPI, ao receber uma mensagem que inclui um anexo TNEF, recuperem as propriedades do anexo.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |TNEF.h  <br/> |
|Expostos pelo:  <br/> |Objetos TNEF  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de transporte, provedores de armazenamento de mensagem e gateways  <br/> |
|Identificador de interface:  <br/> |IID_ITNEF  <br/> |
|Tipo de ponteiro:  <br/> |LPTNEF  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[AddProps](itnef-addprops.md) <br/> |Permite que o provedor de serviços de chamada ou gateway adicionar propriedades ao encapsulamento de uma mensagem ou um anexo.  <br/> |
|[ExtractProps](itnef-extractprops.md) <br/> |Extrai as propriedades de um encapsulamento TNEF.  <br/> |
|[Finish](itnef-finish.md) <br/> |Tiver terminado de processamento de todas as operações de TNEF que estão enfileiradas e em espera.  <br/> |
|[OpenTaggedBody](itnef-opentaggedbody.md) <br/> |Abre uma interface de fluxo no texto de uma mensagem encapsulado.  <br/> |
|[SetProps](itnef-setprops.md) <br/> |Define o valor de uma ou mais propriedades para uma mensagem encapsulada ou um anexo sem modificar a mensagem original ou um anexo.  <br/> |
|[EncodeRecips](itnef-encoderecips.md) <br/> |Codifica um modo de exibição da tabela do destinatário da mensagem o fluxo de dados TNEF da mensagem.  <br/> |
|[FinishComponent](itnef-finishcomponent.md) <br/> |Processa os componentes individuais de uma mensagem de um por vez em um fluxo TNEF.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

