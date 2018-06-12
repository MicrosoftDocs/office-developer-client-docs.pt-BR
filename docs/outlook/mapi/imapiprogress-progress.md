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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 2a003be35fc9c3ef8efc7c66997ee99f6e578f09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767132"
---
# <a name="imapiprogressprogress"></a>IMAPIProgress::Progress

  
  
**Aplica-se a**: Outlook 
  
Atualiza o indicador de progresso com uma exibição do progresso da conforme ele é feito rumo à conclusão da operação. 
  
```cpp
HRESULT Progress(
  ULONG ulValue,
  ULONG ulCount,
  ULONG ulTotal
);
```

## <a name="parameters"></a>Par�metros

 _ulValue_
  
> [in] Um número que indica o nível atual de progresso (calculado a partir dos parâmetros _ulCount_ e _ulTotal_ ou os parâmetros _lpulMin_ e _lpulMax_ do método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) ) entre o modelo global limite inferior e o limite superior global. 
    
 _ulCount_
  
> [in] Um número que indica o item atualmente processado em relação ao total.
    
 _ulTotal_
  
> [in] O número total de itens a serem processados durante a operação.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O indicador de progresso foi atualizado com êxito.
    
## <a name="notes-to-implementers"></a>Notas para implementadores

O parâmetro _ulValue_ será igual ao valor mínimo global apenas no início da operação e ao valor máximo global apenas na conclusão da operação. 
  
Use os parâmetros _ulCount_ e _ulTotal_ , se disponível, para exibir uma mensagem opcional, como "5 itens concluída fora de 10." Se _ulCount_ e _ulTotal_ estiver definidas como 0, decida se alterar visualmente o indicador de progresso. Alguns provedores de serviços definir esses parâmetros como 0 para indicar que eles são processando um Subobjeto cujo andamento é monitorado em relação um objeto pai. Nessa situação, faz sentido para alterar a exibição somente quando o objeto pai relata o progresso. Alguns provedores de serviços passam 0 para esses parâmetros de cada vez. 
  
Para obter mais informações sobre como implementar o **progresso** e outros métodos [IMAPIProgress](imapiprogressiunknown.md) , consulte [Implementando um indicador de progresso](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Notas para chamadores

Nem todos os três dos parâmetros para **IMAPIProgress::Progress** são necessários. O único parâmetro necessário é _ulValue_, um número que indica a porcentagem de progresso. Se o sinalizador MAPI_TOP_LEVEL estiver definido, você também pode passar uma contagem de objetos e um total de objeto. Algumas implementações usam esses valores para exibir uma frase como "5 itens concluída fora de 10" com o indicador de progresso. 
  
Se você estiver copiando todas as mensagens em uma única pasta, defina _ulTotal_ como o número total de mensagens que está sendo copiada. Se você estiver copiando uma pasta, defina _ulTotal_ ao número de subpastas na pasta. Se a pasta a ser copiado não contiver nenhum subpastas e somente as mensagens, defina _ulTotal_ como 1. 
  
Para obter mais informações sobre como e quando fazer chamadas para um objeto de progresso, consulte [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::Progress  <br/> |MFCMAPI usa o método **IMAPIProgress::Progress** para atualizar a barra de status MFCMAPI com a porcentagem atual de andamento, calculado a partir do _uValue_ e os valores máximo e mínimos atuais.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress: IUnknown](imapiprogressiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Exibir um indicador de progresso](how-to-display-a-progress-indicator.md)
  
[Implementando um indicador de progresso](implementing-a-progress-indicator.md)

