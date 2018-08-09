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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 9a6ab96a70bce622f44de6576e7b77861302de4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766997"
---
# <a name="imapiformshutdownform"></a>IMAPIForm::ShutdownForm

  
  
**Aplica-se a**: Outlook 
  
Fecha o formulário.
  
```cpp
HRESULT ShutdownForm(
  ULONG ulSaveOptions
);
```

## <a name="parameters"></a>Parâmetros

 _ulSaveOptions_
  
> [in] Um valor que controla como ou se os dados do formulário são salvos antes que o formulário é fechado. Um dos sinalizadores a seguir pode ser definido:
    
SAVEOPTS_NOSAVE 
  
> Dados do formulário não devem ser salvo.
    
SAVEOPTS_PROMPTSAVE 
  
> O usuário deve ser solicitado a salvar os dados alterados no formulário.
    
SAVEOPTS_SAVEIFDIRTY 
  
> Dados do formulário devem ser salvo se tiver sido alterado desde a última salvar. Se nenhuma interface de usuário que está sendo exibido, o formulário opcionalmente pode alternar para usar a funcionalidade para a opção SAVEOPTS_NOSAVE.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O formulário foi fechado.
    
E_UNEXPECTED 
  
> O formulário já foi fechado por uma chamada anterior ao **ShutdownForm**.
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chame o método **IMAPIForm::ShutdownForm** para fechar um formulário. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Execute as seguintes tarefas na sua implementação de **ShutdownForm**:
  
1. Verifique se um visualizador já não chamado **ShutdownForm**e retornar E_UNEXPECTED se ele tiver sido definido. Embora esta seja improvável, você deve verificar.
    
2. Chame o método de [AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) do seu formulário para que o armazenamento para o formulário e qualquer estruturas de dados internos permaneça disponível até que o processamento está concluído. 
    
3. Determine se há quaisquer alterações não salvas os dados do formulário. Salve os dados de acordo com como o parâmetro _ulSaveOptions_ é definido chamando o método de [IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md) do seu visualizador. 
    
4. Destrua a janela de interface de usuário do seu formulário.
    
5. Libere mensagem e os objetos de site de seu formulário chamando os métodos [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) . 
    
6. Notifica registrados todos os visualizadores do desligamento pendente chamando os métodos [IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md) . 
    
7. Chame o método [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) para cancelar o registro do formulário para fins de notificação, definindo o ponteiro de coletor de eventos advise como **Nulo**.
    
8. Chame a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar a memória para as propriedades do formulário. 
    
9. Chame o método de **IUnknown:: Release** do seu formulário, correspondentes a chamada **AddRef** feita na etapa 2. 
    
10. Retorne S_OK.
    
> [!NOTE]
> Depois que essas ações tenham sido concluídas, os métodos só é válidos no objeto de formulário que podem ser chamadas são aqueles da interface [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando **ShutdownForm** retorna, independentemente se ele retornará um erro, libere o formulário chamando seu método **IUnknown:: Release** . Você pode ignorar com segurança os erros retornados pelo **ShutdownForm**.
  
## <a name="see-also"></a>Confira também



[IMAPIMessageSite::SaveMessage](imapimessagesite-savemessage.md)
  
[IMAPIViewAdviseSink::OnShutdown](imapiviewadvisesink-onshutdown.md)
  
[IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)

