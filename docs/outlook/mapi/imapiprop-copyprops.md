---
title: IMAPIPropCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyProps
api_type:
- COM
ms.assetid: f65da1c8-d49b-44e8-8c66-9c53d088d334
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7319f1abb4a74ee17b0a4a1220215c29434d256b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345504"
---
# <a name="imapipropcopyprops"></a>IMAPIProp::CopyProps

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia ou move as propriedades selecionadas. 
  
```cpp
HRESULT CopyProps(
  LPSPropTagArray lpIncludeProps,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  LPCIID lpInterface,
  LPVOID lpDestObj,
  ULONG ulFlags,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parâmetros

 _lpIncludeProps_
  
> no Um ponteiro para uma matriz de marca de propriedade que especifica as propriedades a serem copiadas ou movidas. **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) não pode ser incluído na matriz. O parâmetro _lpIncludeProps_ não pode ser **nulo**.
    
 _ulUIParam_
  
> no Uma alça para a janela pai do indicador de progresso. 
    
 _lpProgress_
  
> no Um ponteiro para uma implementação de um indicador de progresso. Se **NULL** for passado no parâmetro _lpProgress_ , o indicador de progresso será exibido usando a implementação MAPI. O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MAPI_DIALOG esteja definido no parâmetro _parâmetroulflags_ . 
    
 _lpInterface_
  
> no Um ponteiro para o identificador de interface (IID) que representa a interface que deve ser usada para acessar o objeto apontado pelo parâmetro _lpDestObj_ . O parâmetro _lpInterface_ não deve ser **nulo**.
    
 _lpDestObj_
  
> no Um ponteiro para o objeto para receber as propriedades copiadas ou movidas.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controlam a operação de cópia ou movimentação. Os seguintes sinalizadores podem ser definidos:
    
MAPI_DECLINE_OK 
  
> Se **CopyProps** chama o método [IMAPISupport::D ocopyprops](imapisupport-docopyprops.md) para manipular a operação de cópia ou movimentação, ele deve retornar imediatamente com o valor de erro MAPI_E_DECLINE_COPY. O sinalizador MAPI_DECLINE_OK é definido por MAPI para limitar a recursividade. Os clientes não definem esse sinalizador. 
    
MAPI_DIALOG 
  
> Exibe um indicador de progresso.
    
MAPI_MOVE 
  
> **CopyProps** deve executar uma operação de movimentação em vez de uma operação de cópia. Quando esse sinalizador não é definido, o **CopyProps** realiza uma operação de cópia. 
    
MAPI_NOREPLACE 
  
> As propriedades existentes no objeto de destino não devem ser substituídas. Quando esse sinalizador não é definido, **CopyProps** substitui as propriedades existentes. 
    
 _lppProblems_
  
> [in, out] Na entrada, um ponteiro para um ponteiro para uma estrutura [SPropProblemArray](spropproblemarray.md) ; caso contrário, **NULL**, indicando que não há necessidade de informações de erro. Se _lppProblems_ for um ponteiro válido na entrada, **CopyProps** retornará informações detalhadas sobre erros ao copiar uma ou mais propriedades. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As propriedades foram copiadas ou movidas com êxito.
    
MAPI_E_COLLISION 
  
> Um subobjeto não pode ser copiado porque um subobjeto com o mesmo nome de exibição, definido pela propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), já existe no objeto de destino. 
    
MAPI_E_DECLINE_COPY 
  
> O provedor de serviços não implementa a operação de cópia.
    
MAPI_E_FOLDER_CYCLE 
  
> O objeto de origem executando a operação copiar ou mover direta ou indiretamente contém o objeto de destino. Um trabalho significativo pode ter sido realizado antes da descoberta dessa condição, portanto, os objetos de origem e de destino podem ser parcialmente modificados. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> A interface identificada pelo parâmetro _lpInterface_ não é suportada pelo objeto de destino. 
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de acessar um objeto para o qual o chamador tem permissões insuficientes. Esse erro será retornado se o objeto de destino for o mesmo que o objeto de origem.
    
Os valores a seguir podem ser retornados na estrutura **SPropProblemArray** , mas não como valores de retorno para **CopyProps**. Esses erros se aplicam a uma única propriedade.
  
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e o **CopyProps** não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e **CopyProps** suporta apenas Unicode. 
    
MAPI_E_COMPUTED 
  
> A propriedade não pode ser modificada pelo chamador porque é uma propriedade somente leitura, calculada pelo proprietário do objeto de destino. Esse erro não é grave; o chamador deve permitir que a operação de cópia continue.
    
MAPI_E_INVALID_TYPE 
  
> O tipo de propriedade é inválido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> O tipo de propriedade não é o tipo esperado pelo chamador.
    
## <a name="remarks"></a>Comentários

O método **IMAPIProp:: CopyProps** copia ou move as propriedades selecionadas do objeto atual para um objeto de destino. O **CopyProps** é usado principalmente para responder e encaminhar mensagens, onde apenas algumas das propriedades da mensagem original viajam com a resposta ou a cópia encaminhada. 
  
Todos os subobjetos no objeto de origem são automaticamente incluídos na operação e copiados ou movidos em sua totalidade, independentemente do uso de propriedades indicadas pela estrutura [SPropTagArray](sproptagarray.md) . Por padrão, **CopyProps** substitui quaisquer propriedades no objeto de destino que correspondam às propriedades do objeto de origem. Se qualquer uma das propriedades copiadas ou movidas já existir no objeto de destino, as propriedades existentes serão sobrescritas pelas novas propriedades, a menos que o sinalizador MAPI_NOREPLACE seja definido no parâmetro _parâmetroulflags_ . As informações existentes no objeto de destino que não estão sobrescritas são deixadas inalteradas. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Você pode fornecer uma implementação completa do **CopyProps** ou depender da implementação que a MAPI fornece em seu objeto support. Se você quiser usar a implementação MAPI, chame o método **IMAPISupport::D ocopyprops** . No enTanto, se você fizer o processamento de representante para o **DoCopyProps** e passar o sinalizador MAPI_DECLINE_OK, evite a chamada de suporte e retorne MAPI_E_DECLINE_COPY em vez disso. Você será chamado com este sinalizador por MAPI para evitar a possível recursão que pode ocorrer ao copiar pastas. 
  
Como a operação de cópia pode ser demorada, você deve exibir um indicador de progresso. Use a implementação [método imapiprogress](imapiprogressiunknown.md) que é passada no parâmetro _lpProgress_ , se houver um. Se _lpProgress_ for **NULL**, chame o método [IMAPISupport::D OPROGRESSDIALOG](imapisupport-doprogressdialog.md) para usar a implementação MAPI. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Não defina o sinalizador MAPI_DECLINE_OK; Ele é usado por MAPI em suas chamadas para as implementações de provedor do repositório de mensagens **CopyProps** . 
  
Como as operações de cópia e movimentação podem levar tempo, é prudente solicitar a exibição de um indicador de progresso Configurando o sinalizador MAPI_DIALOG. Você pode definir o parâmetro _lpProgress_ para sua implementação do **método imapiprogress**, se você tiver um, ou como **nulo**. Se _lpProgress_ for **nulo**, **CopyProps** usará o indicador de progresso padrão fornecido por MAPI. 
  
Você pode suprimir a exibição de um indicador de progresso não definindo o sinalizador MAPI_DIALOG. **CopyProps** ignorará os parâmetros _ulUIParam_ e _lpProgress_ e evitará a exibição do indicador. 
  
 **CopyProps** pode relatar erros globais e individuais, ou erros que ocorrem com uma ou mais propriedades. Esses erros individuais são colocados em uma estrutura **SPropProblemArray** . Você pode suprimir o relatório de erros no nível da propriedade passando **NULL**, em vez de um ponteiro válido, para o parâmetro da estrutura da matriz do problema da propriedade. 
  
Se você quiser receber informações sobre erros, passe um ponteiro de estrutura **SPropProblemArray** válido no parâmetro _lppProblems_ . Quando **CopyProps** retorna S_OK, verifique se há possíveis erros com propriedades individuais na estrutura. Quando **CopyProps** retorna um erro, nenhuma informação é retornada na estrutura **SPropProblemArray** . Em vez disso, chame o método [IMAPIProp:: GetLastError](imapiprop-getlasterror.md) para recuperar informações de erro detalhadas. 
  
Se **CopyProps** retornar S_OK, libere a estrutura **SPropProblemArray** retornada chamando a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Se você estiver copiando propriedades que são exclusivas para o tipo de objeto de origem, você deve verificar se o objeto de destino é do mesmo tipo. O **CopyProps** não impede que você associe propriedades que normalmente pertencem a um tipo de objeto com outro tipo de objeto. Você pode copiar propriedades que fazem sentido para o objeto de destino. Por exemplo, você não deve copiar as propriedades de mensagem para um contêiner de catálogo de endereços. 
  
Para garantir que você esteja copiando entre objetos do mesmo tipo, verifique se o objeto de origem e destino são do mesmo tipo, comparando ponteiros de objeto ou chamando o método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) . Defina o identificador de interface apontado por _lpInterface_ para a interface padrão do objeto de origem. Além disso, verifique se o tipo de objeto ou a propriedade **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) é o mesmo para os dois objetos. Por exemplo, se você estiver copiando de uma mensagem, defina _lpInterface_ como IID_IMessage e o **PR_OBJECT_TYPE** para ambos os objetos como MAPI_MESSAGE. 
  
Se um ponteiro inválido for passado no parâmetro _lpDestObj_ , os resultados serão imprevisíveis. 
  
Para copiar a lista de destinatários de uma mensagem, chame o método **CopyProps** da mensagem e inclua a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) na matriz de marca de propriedade. Para copiar os anexos da mensagem, inclua a propriedade **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). 
  
Para copiar uma pasta ou uma tabela de conteúdo ou hierarquia do contêiner de catálogo de endereços, inclua as propriedades **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) no matriz de marca de propriedade. Para incluir a tabela de conteúdo associado de uma pasta, inclua a propriedade **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) na matriz. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |CopyNamedProps  <br/> |MFCMAPI usa o método **IMAPIProp:: CopyProps** para copiar propriedades nomeadas de uma mensagem para outra.  <br/> |
|SingleMAPIPropListCtrl. cpp  <br/> |CSingleMAPIPropListCtrl:: onPasteproperty  <br/> |MFCMAPI usa o método **IMAPIProp:: CopyProps** para colar uma propriedade que foi copiada de outro objeto.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPIProp::CopyTo](imapiprop-copyto.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPISupport::DoCopyProps](imapisupport-docopyprops.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriedade canônica PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Propriedade canônica PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Propriedade canônica PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Propriedade canônica PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)
  
[Propriedade canônica PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Propriedade canônica PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[Propriedade canônica PidTagObjectType](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

