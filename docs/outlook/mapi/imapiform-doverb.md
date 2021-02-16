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
ms.openlocfilehash: 60a8c89afe0d70a1737c6ce694c66359fd6aae4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329453"
---
# <a name="imapiformdoverb"></a>IMAPIForm::DoVerb

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Solicita que o formulário execute as tarefas associadas a um verbo específico.
  
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
  
> [in] Um ponteiro para um objeto de contexto de exibição. O _parâmetro lpViewContext_ pode ser **nulo.**
    
 _hwndParent_
  
> [in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe. O  _parâmetro hwndParent_ deve ser **nulo se** a caixa de diálogo ou a janela não for modal. 
    
 _lprcPosRect_
  
> [in] Um ponteiro para uma estrutura [de RECT](https://msdn.microsoft.com/library/dd162897%28VS.85%29.aspx) Win32 que contém o tamanho e a posição da janela do formulário. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O verbo foi invocado com êxito.
    
OLEOBJ_S_CANNOT_DOVERB_NOW 
  
> O verbo representado pelo parâmetro  _iVerb_ é válido, mas o formulário não pode executar as operações atualmente associadas a ele. 
    
## <a name="remarks"></a>Comentários

Visualizadores de formulário chamam o método **IMAPIForm::D oVerb** para solicitar que o formulário execute as tarefas que ele associa a cada verbo que o formulário suporta. 
  
Cada um dos verbos com suporte é identificado por um valor numérico, passado para **o DoVerb** no _parâmetro iVerb._ Implementações típicas **do DoVerb** contêm uma instrução **de** opção que testa os valores válidos para o  _parâmetro iVerb_ para o formulário. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

If the form viewer specifies a view context in the  _lpViewContext_ parameter, use it in your **DoVerb** implementation instead of the view context passed in an earlier call to the [IMAPIForm::SetViewContext](imapiform-setviewcontext.md) method. Faça as alterações necessárias às suas estruturas de dados internas e não salve o contexto de exibição. 
  
Execute as seguintes tarefas em sua **implementação do DoVerb:** 
  
- Execute qualquer código necessário para o verbo específico associado ao _parâmetro iVerb._ 
    
- Se necessário, restaure o contexto do modo de exibição original.
    
- Se um número de verbo desconhecido for passado, retorne MAPI_E_NO_SUPPORT. Caso contrário, retorne um resultado com base no sucesso ou falha de qualquer verbo que tenha sido executado.
    
- Feche o formulário. É sempre sua responsabilidade fechar o formulário após a conclusão de uma chamada **do DoVerb.** 
    
Alguns verbos, como Print, devem ser modais em relação à chamada **do DoVerb** — ou seja, a operação indicada deve ser concluída antes que a chamada **do DoVerb** seja retornada. 
  
Para obter a **estrutura RECT** usada pela janela de um formulário, chame a [função GetWindowRect.](https://msdn.microsoft.com/library/ms633519) 
  
Não salve o alça no parâmetro  _hwndParent_ porque, embora ele normalmente permaneça válido até a conclusão do **DoVerb,** ele pode ser destruído imediatamente após o retorno da chamada.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Você pode fazer verbos não modais atuarem como verbos modais apontando _lpViewContext_ para uma implementação de contexto de exibição que retorna o sinalizador VCSTATUS_MODAL de seu método [IMAPIViewContext::GetViewStatus.](imapiviewcontext-getviewstatus.md) 
  
Para obter mais informações sobre verbos em MAPI, consulte [Verbos de formulário.](form-verbs.md) Para obter mais informações sobre como os verbos são tratados no OLE, consulte [OLE e Transferência de Dados.](https://msdn.microsoft.com/library/ms693425%28VS.85%29.aspx)
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::CallDoVerb  <br/> |MFCMAPI usa o **método IMAPIForm::D oVerb** para invocar um verbo em um formulário.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIForm::SetViewContext](imapiform-setviewcontext.md)
  
[IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Verbos de formulário](form-verbs.md)

