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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d3b47e423daf428c67761d13deef1ae0858c91c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280199"
---
# <a name="imapicontrolactivate"></a>IMAPIControl::Activate

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Executa uma tarefa, como exibir uma caixa de diálogo ou iniciar uma operação programática quando um usuário de aplicativo cliente clica no controle de botão.
  
```cpp
HRESULT Activate(
  ULONG ulFlags,
  ULONG_PTR ulUIParam
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Serve deve ser zero.
    
 _ulUIParam_
  
> no Uma alça para a janela pai da caixa de diálogo na qual o controle Button aparece.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O controle de botão foi ativado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPIControl:: Activate** executa tarefas após o clique do controle de botão de um usuário. Depois que o clique ocorre, como parte do processamento da tabela de exibição, o MAPI faz uma chamada para **Activate** após chamar [IMAPIControl:: GetState](imapicontrol-getstate.md) para determinar se o botão está habilitado. 
  
Para obter mais informações sobre como implementar **Activate** e os outros métodos [IMAPIControl: IUnknown](imapicontroliunknown.md) , consulte [Control Object Implementation](control-object-implementation.md).
  
## <a name="see-also"></a>Confira também



[IMAPIControl::GetState](imapicontrol-getstate.md)
  
[IMAPIControl : IUnknown](imapicontroliunknown.md)

