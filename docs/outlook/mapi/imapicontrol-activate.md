---
title: IMAPIControlActivate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIControl.Activate
api_type:
- COM
ms.assetid: 2b641030-2429-4217-a648-0a9f3d1a1b29
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: fb6cd23acdb81af250e7e6dfe6facf7226850363
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766938"
---
# <a name="imapicontrolactivate"></a>IMAPIControl::Activate

  
  
**Aplica-se a**: Outlook 
  
Executa uma tarefa como exibir uma caixa de diálogo ou iniciar uma operação programática quando um usuário do aplicativo cliente clica no controle de botão.
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _ulUIParam_
  
> [in] Uma alça para a janela pai da caixa de diálogo na qual o controle de botão aparece.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O controle de botão foi ativado com êxito.
    
## <a name="remarks"></a>Coment�rios

O método **IMAPIControl::Activate** executa tarefas após o clique de um usuário do controle de botão. Após o clique ocorre, como parte do processamento da tabela exibição, o MAPI faz uma chamada para **Ativar** após a primeira chamada [IMAPIControl::GetState](imapicontrol-getstate.md) para determinar se o botão está habilitado. 
  
Para obter mais informações sobre como implementar **Ativar** e o outro [IMAPIControl: IUnknown](imapicontroliunknown.md) métodos, consulte a [Implementação do objeto de controle](control-object-implementation.md).
  
## <a name="see-also"></a>Confira também



[IMAPIControl::GetState](imapicontrol-getstate.md)
  
[IMAPIControl: IUnknown](imapicontroliunknown.md)

