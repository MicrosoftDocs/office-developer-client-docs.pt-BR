---
title: IMAPIFormDoVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.DoVerb
api_type:
- COM
ms.assetid: 8b582571-b448-4476-91d9-4cc94dbec710
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fe6270d82d227f52dfd5dfa5454c73e815ad9f42
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573814"
---
# <a name="imapiformdoverb"></a>IMAPIForm::DoVerb

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Solicita que o formulário execute qualquer item das tarefas ele associa um verbo específico.
  
```cpp
HRESULT DoVerb(
  LONG iVerb,
  LPMAPIVIEWCONTEXT lpViewContext,
  ULONG_PTR hwndParent,
  LPCRECT lprcPosRect
);
```

## <a name="parameters"></a>Parâmetros

 _iVerb_
  
> [in] O número associado a um dos verbos do formulário.
    
 _lpViewContext_
  
> [in] Um ponteiro para um objeto de contexto do modo de exibição. O parâmetro _lpViewContext_ pode ser **nula**.
    
 _hwndParent_
  
> [in] Um identificador para a janela do pai de quaisquer caixas de diálogo ou windows esse método exibe. O parâmetro _hwndParent_ deve ser **Nulo** se a caixa de diálogo ou a janela não é modal. 
    
 _lprcPosRect_
  
> [in] Um ponteiro para um Win32 estrutura [Retangular](http://msdn.microsoft.com/en-us/library/dd162897%28VS.85%29.aspx) que contém o tamanho e a posição da janela do formulário. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O verbo com êxito foi invocado.
    
OLEOBJ_S_CANNOT_DOVERB_NOW 
  
> O verbo representado pelo parâmetro _iVerb_ é válido, mas o formulário não é possível executar as operações atualmente associadas a ela. 
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chame o método de **IMAPIForm::DoVerb** para solicitar que o formulário execute as tarefas que ela associa a cada verbo que o formulário oferece suporte. 
  
Cada um dos verbos com suporte é identificado por um valor numérico, passado para **DoVerb** no parâmetro _iVerb_ . Implementações típicas dos **DoVerb** contenham uma instrução **switch** que testa os valores válidos para o parâmetro _iVerb_ para o formulário. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Se a tela de formulário especifica um contexto de modo de exibição no parâmetro _lpViewContext_ , usá-lo na sua implementação **DoVerb** em vez do contexto de modo de exibição passada em uma chamada anterior para o método [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) . Fazer as alterações necessárias para suas estruturas de dados interno e não salve o contexto de modo de exibição. 
  
Execute as seguintes tarefas na sua implementação **DoVerb** : 
  
- Execute qualquer código é necessário para o verbo específico que está associado com o parâmetro _iVerb_ . 
    
- Se necessário, restaure o contexto de modo de exibição original.
    
- Se um número de verbo desconhecido foi passado, retorne MAPI_E_NO_SUPPORT. Caso contrário, retornar um resultado baseado no sucesso ou falha de qualquer verbo foi executada.
    
- Feche o formulário. É sempre fechar o formulário após a conclusão de uma chamada **DoVerb** sua responsabilidade. 
    
Alguns verbos, como imprimir, devem ser modais com relação a chamada **DoVerb** — ou seja, a operação indicada deve ser concluída antes da chamada **DoVerb** retorna. 
  
Para obter a estrutura de **Retangular** usada pela janela de um formulário, chame a função de [GetWindowRect](http://msdn.microsoft.com/en-us/library/ms633519) . 
  
Não salve a alça no parâmetro _hwndParent_ porque, embora ele geralmente permanecerá válido até a conclusão da **DoVerb**, ele pode ser destruído imediatamente após retornar da chamada.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode fazer com que não restrita verbos agir como verbos modais, apontando _lpViewContext_ para uma implementação de contexto do modo de exibição que retorna o sinalizador VCSTATUS_MODAL de seu método de [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) . 
  
Para obter mais informações sobre os verbos na MAPI, consulte [Verbos de formulário](form-verbs.md). Para obter mais informações sobre como os verbos são manipulados no OLE, consulte [OLE e transferência de dados](http://msdn.microsoft.com/en-us/library/ms693425%28VS.85%29.aspx).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CallDoVerb  <br/> |MFCMAPI usa o método **IMAPIForm::DoVerb** para invocar um verbo em um formulário.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIForm::SetViewContext](imapiform-setviewcontext.md)
  
[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Verbos de formulário](form-verbs.md)

