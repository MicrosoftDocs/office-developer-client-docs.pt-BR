---
title: IMAPIProgressProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.Progress
api_type:
- COM
ms.assetid: edbf7623-a64e-43b8-8379-e3cde2433d91
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3cf639286a504b9edb600214d13dbe50710e76a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435492"
---
# <a name="imapiprogressprogress"></a>IMAPIProgress::Progress

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Atualiza o indicador de progresso com uma exibição do progresso conforme ele é feito na conclusão da operação. 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a>Parâmetros

 _ulValue_
  
> no Um número que indica o nível atual de progresso (calculado a partir dos parâmetros _ulCount_ e _ulTotal_ ou dos parâmetros _LpulMin_ e _LpulMax_ do método [método imapiprogress::](imapiprogress-setlimits.md) setlimits) entre o global limite inferior e o limite superior global. 
    
 _ulCount_
  
> no Um número que indica o item atualmente processado relativo ao total.
    
 _ulTotal_
  
> no O número total de itens a serem processados durante a operação.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O indicador de progresso foi atualizado com êxito.
    
## <a name="notes-to-implementers"></a>Observações para implementadores

O parâmetro _ulValue_ será igual ao valor global mínimo somente no início da operação e no valor global máximo apenas na conclusão da operação. 
  
Use os parâmetros _ulCount_ e _ulTotal_ , se estiver disponível, para exibir uma mensagem opcional, como "5 itens concluídos de 10". Se _ulCount_ e _ulTotal_ estiverem definidos como 0, decida se você deve alterar visualmente o indicador de progresso. Alguns provedores de serviços definem esses parâmetros como 0 para indicar que estão processando um subobjeto cujo andamento é monitorado em relação a um objeto pai. Nessa situação, faz sentido alterar a exibição somente quando o objeto pai relata o progresso. Alguns provedores de serviços passam 0 para esses parâmetros a cada vez. 
  
Para obter mais informações sobre como implementar o **progresso** e os outros métodos do [método imapiprogress](imapiprogressiunknown.md) , consulte [implementando um indicador de progresso](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Notas para chamadores

Nem todos os três parâmetros para **método imapiprogress::P rogress** são necessários. O único parâmetro necessário é _ulValue_, um número que indica a porcentagem de progresso. Se o sinalizador MAPI_TOP_LEVEL estiver definido, você também pode passar uma contagem de objeto e um total de objeto. Algumas implementações usam esses valores para exibir uma frase como "5 itens concluídos de 10" com o indicador de progresso. 
  
Se você estiver copiando todas as mensagens em uma única pasta, defina _ulTotal_ para o número total de mensagens que estão sendo copiadas. Se você estiver copiando uma pasta, defina _ulTotal_ para o número de subpastas na pasta. Se a pasta a ser copiada não contiver subpastas e somente mensagens, defina _ulTotal_ como 1. 
  
Para saber mais sobre como e quando fazer chamadas para um objeto de progresso, confira o tópico [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::P rogress  <br/> |MFCMAPI usa o método **método imapiprogress::P rogress** para atualizar a barra de status do MFCMAPI com a porcentagem atual de progresso, calculada de _uValue_ e os valores máximo e mínimo atuais.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Exibir um indicador de progresso](how-to-display-a-progress-indicator.md)
  
[Como implementar um indicador de progresso](implementing-a-progress-indicator.md)

