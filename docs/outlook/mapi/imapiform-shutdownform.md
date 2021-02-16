---
title: IMAPIFormShutdownForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.ShutdownForm
api_type:
- COM
ms.assetid: f1e2a526-40ad-4a93-908f-8ab9a65928a8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 073a76766a296d86e7a23809921b832d494a8f1b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329474"
---
# <a name="imapiformshutdownform"></a>IMAPIForm::ShutdownForm

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fecha o formulário.
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a>Parâmetros

 _ulSaveOptions_
  
> [in] Um valor que controla como ou se os dados no formulário são salvos antes de o formulário ser fechado. Um dos sinalizadores a seguir pode ser definido:
    
SAVEOPTS_NOSAVE 
  
> Os dados do formulário não devem ser salvos.
    
SAVEOPTS_PROMPTSAVE 
  
> O usuário deve ser solicitado a salvar quaisquer dados alterados no formulário.
    
SAVEOPTS_SAVEIFDIRTY 
  
> Os dados do formulário devem ser salvos se eles foram alterados desde o último salvar. Se nenhuma interface do usuário estiver sendo exibida, o formulário pode, opcionalmente, alternar para usar a funcionalidade para a SAVEOPTS_NOSAVE opção.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O formulário foi fechado.
    
E_UNEXPECTED 
  
> O formulário já foi fechado por uma chamada anterior para **ShutdownForm**.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chamam **o método IMAPIForm::ShutdownForm** para fechar um formulário. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Execute as seguintes tarefas na implementação do **ShutdownForm:**
  
1. Verifique se um visualizador ainda não chamou **ShutdownForm** e retorne E_UNEXPECTED se tiver sido. Embora isso seja improvável, você deve verificar.
    
2. Chame o método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) do formulário para que o armazenamento do formulário e de todas as estruturas de dados internas permaneçam disponíveis até que o processamento seja concluído. 
    
3. Determine se há alguma alteração não sedada nos dados do formulário. Salve dados não salvo de acordo com o modo como o  _parâmetro ulSaveOptions_ é definido chamando o método [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) do visualizador. 
    
4. Destruir a janela da interface do usuário do formulário.
    
5. Libere os objetos de site de mensagem e mensagem do formulário chamando seus métodos [IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) 
    
6. Notifique todos os visualizadores registrados sobre o desligamento pendente chamando seus métodos [IMAPIViewAdviseSink::OnShutdown.](imapiviewadvisesink-onshutdown.md) 
    
7. Chame o [método IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) para cancelar o registro do seu formulário para notificação definindo o ponteiro do pia de aviso como **nulo.**
    
8. Chame a [função MAPIFreeBuffer](mapifreebuffer.md) para liberar a memória para as propriedades do seu formulário. 
    
9. Chame o método **IUnknown::Release** do formulário, correspondendo à chamada **AddRef** feita na etapa 2. 
    
10. Retorne S_OK.
    
> [!NOTE]
> Depois que essas ações foram concluídas, os únicos métodos válidos no objeto de formulário que podem ser chamados são aqueles da interface [IUnknown.](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando **ShutdownForm** retornar, independentemente de retornar um erro, libere o formulário chamando seu **método IUnknown::Release.** Você pode ignorar com segurança quaisquer erros retornados pelo **ShutdownForm**.
  
## <a name="see-also"></a>Confira também



[IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)
  
[IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

