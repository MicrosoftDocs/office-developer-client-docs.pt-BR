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
  
> [in] Um ponteiro para uma matriz de marca de propriedade que especifica as propriedades a copiar ou mover. **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) não pode ser incluído na matriz. O _parâmetro lpIncludeProps_ não pode ser **nulo.**
    
 _ulUIParam_
  
> [in] Um alça para a janela pai do indicador de progresso. 
    
 _lpProgress_
  
> [in] Um ponteiro para uma implementação de um indicador de progresso. Se **nulo** for passado no  _parâmetro lpProgress,_ o indicador de progresso será exibido usando a implementação de MAPI. O _parâmetro lpProgress_ é ignorado, a menos que o sinalizador MAPI_DIALOG seja definido no _parâmetro ulFlags._ 
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface que deve ser usada para acessar o objeto apontado pelo parâmetro _lpDestObj._ O _parâmetro lpInterface_ não deve ser **nulo.**
    
 _lpDestObj_
  
> [in] Um ponteiro para o objeto para receber as propriedades copiadas ou movidas.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla a operação de cópia ou movimentação. Os sinalizadores a seguir podem ser definidos:
    
MAPI_DECLINE_OK 
  
> Se **CopyProps** chamar o método [IMAPISupport::D oCopyProps](imapisupport-docopyprops.md) para manipular a operação de cópia ou movimentação, ele deverá retornar imediatamente com o valor de erro MAPI_E_DECLINE_COPY. O MAPI_DECLINE_OK sinalizador é definido por MAPI para limitar a recursão. Os clientes não configuram esse sinalizador. 
    
MAPI_DIALOG 
  
> Exibe um indicador de progresso.
    
MAPI_MOVE 
  
> **CopyProps** deve executar uma operação de movimentação em vez de uma operação de cópia. Quando esse sinalizador não está definido, **CopyProps** executa uma operação de cópia. 
    
MAPI_NOREPLACE 
  
> As propriedades existentes no objeto de destino não devem ser substituídas. Quando esse sinalizador não está definido, **CopyProps** substitui as propriedades existentes. 
    
 _lppProblems_
  
> [in, out] Na entrada, um ponteiro para um ponteiro para uma [estrutura SPropProblemArray;](spropproblemarray.md) caso contrário, **nulo**, indicando que não há necessidade de informações de erro. Se  _lppProblems_ for um ponteiro válido na entrada, **CopyProps** retornará informações detalhadas sobre erros ao copiar uma ou mais propriedades. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As propriedades foram copiadas ou movidas com êxito.
    
MAPI_E_COLLISION 
  
> Um subobjeto não pode ser copiado porque um subobjeto com o mesmo nome de exibição, definido pela propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), já existe no objeto de destino. 
    
MAPI_E_DECLINE_COPY 
  
> O provedor de serviços não implementa a operação de cópia.
    
MAPI_E_FOLDER_CYCLE 
  
> O objeto de origem que executa a operação de cópia ou movimentação direta ou indiretamente contém o objeto de destino. Um trabalho significativo pode ter sido realizado antes dessa condição ser descoberta, portanto, os objetos de origem e destino podem ser parcialmente modificados. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> A interface identificada pelo parâmetro  _lpInterface_ não é suportada pelo objeto de destino. 
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de acessar um objeto para o qual o chamador tem permissões insuficientes. Esse erro será retornado se o objeto de destino for o mesmo que o objeto de origem.
    
Os seguintes valores podem ser retornados na **estrutura SPropProblemArray,** mas não como valores de retorno para **CopyProps**. Esses erros se aplicam a uma única propriedade.
  
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE padrão foi definido e **CopyProps** não dá suporte a Unicode ou MAPI_UNICODE não foi definido e **CopyProps** dá suporte apenas a Unicode. 
    
MAPI_E_COMPUTED 
  
> A propriedade não pode ser modificada pelo chamador porque é uma propriedade somente leitura, calculada pelo proprietário do objeto de destino. Este erro não é grave; o chamador deve permitir que a operação de cópia continue.
    
MAPI_E_INVALID_TYPE 
  
> O tipo de propriedade é inválido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> O tipo de propriedade não é o tipo esperado pelo chamador.
    
## <a name="remarks"></a>Comentários

O **método IMAPIProp::CopyProps** copia ou move propriedades selecionadas do objeto atual para um objeto de destino. **CopyProps** é usado principalmente para responder e encaminhar mensagens, onde apenas algumas das propriedades da mensagem original viajam com a resposta ou a cópia encaminhada. 
  
Quaisquer subobjetos no objeto de origem são incluídos automaticamente na operação e copiados ou movidos em sua totalidade, independentemente do uso das propriedades indicadas pela [estrutura SPropTagArray.](sproptagarray.md) Por padrão, **CopyProps** substitui todas as propriedades no objeto de destino que corresponderem a propriedades do objeto de origem. Se alguma das propriedades copiadas ou movidas já existir no objeto de destino, as propriedades existentes serão substituídas pelas novas propriedades, a menos que o sinalizador MAPI_NOREPLACE seja definido no parâmetro _ulFlags._ As informações existentes no objeto de destino que não são sobrescritas não são deixadas intocadas. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Você pode fornecer uma implementação completa **de CopyProps ou** contar com a implementação que o MAPI fornece em seu objeto de suporte. Se você quiser usar a implementação de MAPI, chame o **método IMAPISupport::D oCopyProps.** No entanto, se você delegar o processamento para **DoCopyProps** e passar o sinalizador MAPI_DECLINE_OK, evite a chamada de suporte e retorne MAPI_E_DECLINE_COPY vez. Você será chamado com esse sinalizador pelo MAPI para evitar a possível recursão que pode ocorrer ao copiar pastas. 
  
Como a operação de cópia pode ser demorada, você deve exibir um indicador de progresso. Use a [implementação IMAPIProgress](imapiprogressiunknown.md) que é passada no parâmetro  _lpProgress,_ se houver uma. Se  _lpProgress_ for **nulo,** chame o [método IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) para usar a implementação de MAPI. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Não definir o MAPI_DECLINE_OK sinalizador; ele é usado pelo MAPI em suas chamadas para implementações do provedor de armazenamento de mensagens **CopyProps.** 
  
Como as operações de copiar e mover podem demorar, é sensato solicitar a exibição de um indicador de progresso definindo o sinalizador MAPI_DIALOG dados. You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**. Se  _lpProgress_ for **nulo,** **CopyProps** usará o indicador de progresso padrão fornecido por MAPI. 
  
Você pode suprimir a exibição de um indicador de progresso não definindo o MAPI_DIALOG sinalizador. **CopyProps** ignorará os  _parâmetros ulUIParam_ e  _lpProgress_ e evitará exibir o indicador. 
  
 **CopyProps** pode relatar erros globais e individuais ou erros que ocorrem com uma ou mais das propriedades. Esses erros individuais são colocados em uma **estrutura SPropProblemArray.** Você pode suprimir o relatório de erros no nível da propriedade passando **nulo**, em vez de um ponteiro válido, para o parâmetro de estrutura da matriz do problema de propriedade. 
  
Se você quiser receber informações sobre erros, passe um ponteiro de estrutura **SPropProblemArray** válido no parâmetro _lppProblems._ Quando **CopyProps** retornar S_OK, verifique se há possíveis erros com propriedades individuais na estrutura. Quando **CopyProps** retorna um erro, nenhuma informação é retornada na **estrutura SPropProblemArray.** Em vez disso, chame [o método IMAPIProp::GetLastError](imapiprop-getlasterror.md) para recuperar informações de erro detalhadas. 
  
Se **CopyProps** retornar S_OK, livre a estrutura **SPropProblemArray** retornada chamando a [função MAPIFreeBuffer.](mapifreebuffer.md) 
  
Se você estiver copiando propriedades que são exclusivas para o tipo de objeto de origem, você deve certificar-se de que o objeto de destino é do mesmo tipo. **CopyProps** não impede que você associe propriedades que normalmente pertencem a um tipo de objeto com outro tipo de objeto. Você pode copiar as propriedades que fazem sentido para o objeto de destino. Por exemplo, você não deve copiar as propriedades da mensagem para um contêiner de livro de endereços. 
  
Para garantir que você está copiando entre objetos do mesmo tipo, verifique se o objeto de origem e de destino são do mesmo tipo, comparando ponteiros de objeto ou chamando o método [IUnknown::QueryInterface.](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d%28Office.15%29.aspx) Definir o identificador de interface apontado por  _lpInterface_ para a interface padrão para o objeto de origem. Além disso, verifique se o tipo de objeto **ou PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) é o mesmo para os dois objetos. Por exemplo, se você estiver copiando de uma mensagem, de definida  _lpInterface_ como IID_IMessage e o **PR_OBJECT_TYPE** para ambos os objetos MAPI_MESSAGE. 
  
Se um ponteiro inválido for passado no  _parâmetro lpDestObj,_ os resultados serão imprevisíveis. 
  
Para copiar a lista de destinatários de uma mensagem, chame o método **CopyProps** da mensagem e inclua a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) na matriz de marca de propriedade. Para copiar os anexos da mensagem, inclua a **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) . 
  
Para copiar a hierarquia ou a tabela de conteúdo de um contêiner de pasta ou de um conjunto de endereços, inclua as propriedades **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) na matriz de marca de propriedade. Para incluir a tabela de conteúdo associada de uma pasta, inclua a propriedade **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) na matriz. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CopyNamedProps  <br/> |MFCMAPI usa o **método IMAPIProp::CopyProps** para copiar propriedades nomeadas de uma mensagem para outra.  <br/> |
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::OnPasteProperty  <br/> |MFCMAPI usa o **método IMAPIProp::CopyProps** para colar uma propriedade que foi copiada de outro objeto.  <br/> |
   
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

