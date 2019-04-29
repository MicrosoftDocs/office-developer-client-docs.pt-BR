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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1f815a914deb5e21f3d913abe46a84cc7a32b4ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428512"
---
# <a name="itnef--iunknown"></a>ITnef : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece métodos para o encapsulamento de propriedades MAPI que não são compatíveis com um sistema de mensagens em fluxos binários que podem ser anexados a mensagens. O formato usado para esse encapsulamento é o formato de encapsulamento de transporte neutro (TNEF). O provedor de transporte de destino ou aplicativo cliente baseado em MAPI pode então, ao receber uma mensagem que inclui um anexo TNEF, recupera as propriedades do anexo.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |TNEF. h  <br/> |
|Exposto por:  <br/> |Objetos TNEF  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de transporte, provedores de repositórios de mensagens e gateways  <br/> |
|Identificador de interface:  <br/> |IID_ITNEF  <br/> |
|Tipo de ponteiro:  <br/> |LPTNEF  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[AddProps](itnef-addprops.md) <br/> |Permite que o provedor de serviços de chamada ou o gateway adicione Propriedades ao encapsulamento de uma mensagem ou de um anexo.  <br/> |
|[ExtractProps](itnef-extractprops.md) <br/> |Extrai as propriedades de um encapsulamento TNEF.  <br/> |
|[Finish](itnef-finish.md) <br/> |Conclui o processamento de todas as operações TNEF que estão na fila e aguardando.  <br/> |
|[OpenTaggedBody](itnef-opentaggedbody.md) <br/> |Abre uma interface de fluxo no texto de uma mensagem encapsulada.  <br/> |
|[SetProps](itnef-setprops.md) <br/> |Define o valor de uma ou mais propriedades de uma mensagem encapsulada ou anexo sem modificar a mensagem original ou o anexo.  <br/> |
|[EncodeRecips](itnef-encoderecips.md) <br/> |Codifica um modo de exibição para a tabela de destinatários de uma mensagem no fluxo de dados TNEF para a mensagem.  <br/> |
|[FinishComponent](itnef-finishcomponent.md) <br/> |Processa componentes individuais de uma mensagem de cada vez em um fluxo TNEF.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

