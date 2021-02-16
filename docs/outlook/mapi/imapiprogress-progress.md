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
  
Atualiza o indicador de progresso com uma exibição do progresso conforme ele é feito na direção da conclusão da operação. 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a>Parâmetros

 _ulValue_
  
> [in] Um número que indica o nível atual de progresso (calculado a partir dos parâmetros  _ulCount_ e  _ulTotal_ ou dos parâmetros  _lpulMin_ e  _lpulMax_ do método [IMAPIProgress::SetLimits)](imapiprogress-setlimits.md) entre o limite inferior global e o limite superior global. 
    
 _ulCount_
  
> [in] Um número que indica o item processado no momento em relação ao total.
    
 _ulTotal_
  
> [in] O número total de itens a serem processados durante a operação.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O indicador de progresso foi atualizado com êxito.
    
## <a name="notes-to-implementers"></a>Observações para implementadores

O  _parâmetro ulValue_ será igual ao valor mínimo global somente no início da operação e ao valor máximo global somente na conclusão da operação. 
  
Use os  _parâmetros ulCount_ e  _ulTotal,_ se disponíveis, para exibir uma mensagem opcional, como "5 itens concluídos em 10". Se  _ulCount_ e  _ulTotal_ são definidos como 0, decida se deve alterar visualmente o indicador de progresso. Alguns provedores de serviços configuram esses parâmetros como 0 para indicar que estão processando um subobjeto cujo progresso é monitorado em relação a um objeto pai. Nessa situação, faz sentido alterar a exibição somente quando o objeto pai relata progresso. Alguns provedores de serviços passam 0 para esses parâmetros sempre. 
  
Para obter mais informações sobre como implementar **o progresso** e os outros [métodos IMAPIProgress,](imapiprogressiunknown.md) consulte [Implementando um indicador de progresso](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Notas para chamadores

Nem todos os três parâmetros para **IMAPIProgress::P ess** são necessários. O único parâmetro necessário é  _ulValue_, um número que indica a porcentagem de progresso. Se o MAPI_TOP_LEVEL sinalizador estiver definido, você também poderá passar uma contagem de objetos e um total de objetos. Algumas implementações usam esses valores para exibir uma frase como "5 itens concluídos em 10" com o indicador de progresso. 
  
Se você estiver copiando todas as mensagens em uma única pasta, de definir  _ulTotal_ como o número total de mensagens sendo copiadas. Se você estiver copiando uma pasta, de definir  _ulTotal_ como o número de subpastas na pasta. Se a pasta a ser copiada não contiver subpastas e apenas mensagens, de definida  _como_ 1. 
  
Para saber mais sobre como e quando fazer chamadas para um objeto de progresso, confira o tópico [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::P ress  <br/> |MFCMAPI usa o método **IMAPIProgress::P ess** para atualizar a barra de status MFCMAPI com a porcentagem atual de progresso, calculada a partir de  _uValue_ e os valores máximo e mínimo atuais.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Exibir um indicador de progresso](how-to-display-a-progress-indicator.md)
  
[Como implementar um indicador de progresso](implementing-a-progress-indicator.md)

