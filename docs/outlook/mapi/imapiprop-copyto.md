---
title: IMAPIPropCopyTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.CopyTo
api_type:
- COM
ms.assetid: e56042e9-5bb7-4a99-b6de-1546d4ca07f0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f76b0a5482647fe3e181a36d7dcd8cb60ffc8985
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356389"
---
# <a name="imapipropcopyto"></a>IMAPIProp::CopyTo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia ou move todas as propriedades, exceto para propriedades especificamente excluídas.
  
```cpp
HRESULT CopyTo(
 ULONG ciidExclude,
 LPCIID rgiidExclude,
 LPSPropTagArray lpExcludeProps,
 ULONG_PTR ulUIParam,
 LPMAPIPROGRESS lpProgress,
 LPCIID lpInterface,
 LPVOID lpDestObj,
 ULONG ulFlags,
 LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parâmetros

 _ciidExclude_
  
> [in] A contagem de interfaces a excluir quando as propriedades são copiadas ou movidas.
    
 _rgiidExclude_
  
> [in] Uma matriz de identificadores de interface (IIDs) que especificam interfaces que não devem ser usadas quando informações complementares são copiadas ou movidas para o objeto de destino.
    
 _lpExcludeProps_
  
> [in] Um ponteiro para uma matriz de marcas de propriedade que identifica as marcas de propriedade que devem ser excluídas da operação de cópia ou movimentação. Passar **nulo** no  _parâmetro lpExcludeProps_ indica que todas as propriedades do objeto devem ser copiadas ou movidas. **CopyTo** retorna MAPI_E_INVALID_PARAMETER quando o membro **cValues** da estrutura [SPropProblemArray](spropproblemarray.md) apontado por  _lpExcludeProps_ é definido como 0. 
    
 _ulUIParam_
  
> [in] Um alça para a janela pai do indicador de progresso. 
    
 _lpProgress_
  
> [in] Um ponteiro para uma implementação do indicador de progresso. Se **nulo** for passado no  _parâmetro lpProgress,_ MAPI fornece a implementação de progresso. O _parâmetro lpProgress_ é ignorado, a menos que o sinalizador MAPI_DIALOG seja definido no _parâmetro ulFlags._ 
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o objeto apontado pelo parâmetro _lpDestObj._ O _parâmetro lpInterface_ não deve ser **nulo.**
    
 _lpDestObj_
  
> [in] Um ponteiro para o objeto para receber as propriedades copiadas ou movidas.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla a operação de cópia ou movimentação. Os sinalizadores a seguir podem ser definidos:
    
MAPI_DECLINE_OK 
  
> Se **CopyTo** chamar o método [IMAPISupport::D oCopyTo](imapisupport-docopyto.md) para manipular a operação de movimentação ou cópia, ele deverá retornar imediatamente com o valor de erro MAPI_E_DECLINE_COPY. O MAPI_DECLINE_OK sinalizador é definido por MAPI para limitar a recursão. Os clientes não configuram esse sinalizador. 
    
MAPI_DIALOG 
  
> Exibe um indicador de progresso.
    
MAPI_MOVE 
  
> **CopyTo** deve executar uma operação de movimentação em vez de uma operação de cópia. Quando esse sinalizador não está definido, **CopyTo** executa uma operação de cópia. 
    
MAPI_NOREPLACE 
  
> As propriedades existentes no objeto de destino não devem ser substituídas. Quando esse sinalizador não estiver definido, **CopyTo** substituirá as propriedades existentes. 
    
 _lppProblems_
  
> [in, out] Na entrada, um ponteiro para um ponteiro para uma **estrutura SPropProblemArray;** caso contrário, **nulo**, indicando que não há necessidade de informações de erro. Se  _lppProblems_ for um ponteiro válido na entrada, **CopyTo** retornará informações detalhadas sobre erros ao copiar uma ou mais propriedades. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As propriedades foram copiadas ou movidas com êxito.
    
MAPI_E_COLLISION 
  
> Um subobjeto não pode ser copiado porque um subobjeto com o mesmo nome de exibição — especificado pela propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) — já existe no objeto de destino. 
    
MAPI_E_DECLINE_COPY 
  
> O provedor de serviços não implementa a operação de cópia.
    
MAPI_E_FOLDER_CYCLE 
  
> O objeto de origem que executa a operação de cópia ou movimentação direta ou indiretamente contém o objeto de destino. Um trabalho significativo pode ter sido realizado antes dessa condição ser descoberta, portanto, os objetos de origem e destino podem ser parcialmente modificados. 
    
MAPI_E_INTERFACE_NOT_SUPPORTED 
  
> A interface identificada pelo parâmetro  _lpInterface_ não é suportada pelo objeto de destino. 
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de acessar um objeto para o qual o chamador tem permissões insuficientes. Esse erro será retornado se o objeto de destino for o mesmo que o objeto de origem.
    
Os seguintes valores podem ser retornados na **estrutura SPropProblemArray,** mas não como valores de retorno para **CopyTo**. Os seguintes erros se aplicam a uma única propriedade:
  
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e **CopyTo** não dá suporte a Unicode ou MAPI_UNICODE não foi definido e **CopyTo** dá suporte apenas a Unicode. 
    
MAPI_E_COMPUTED 
  
> A propriedade não pode ser modificada pelo chamador porque é uma propriedade somente leitura, calculada pelo proprietário do objeto de destino. Este erro não é grave; o chamador deve permitir que a operação de cópia continue.
    
MAPI_E_INVALID_TYPE 
  
> O tipo de propriedade é inválido.
    
MAPI_E_UNEXPECTED_TYPE 
  
> O tipo de propriedade não é o tipo esperado pelo chamador.
    
## <a name="remarks"></a>Comentários

Por padrão, o **método IMAPIProp::CopyTo** copia ou move todas as propriedades do objeto atual para um objeto de destino. **CopyTo** é usado quando um objeto deve ser copiado ou movido exatamente, com todas ou a maioria de suas propriedades intactas. 
  
Quaisquer subobjetos no objeto de origem são incluídos automaticamente na operação e são copiados ou movidos em sua totalidade. Por padrão, **CopyTo** substitui todas as propriedades no objeto de destino que corresponderem a propriedades do objeto de origem. Se alguma das propriedades copiadas ou movidas já existir no objeto de destino, as propriedades existentes serão substituídas pelas novas propriedades, a menos que o sinalizador MAPI_NOREPLACE seja definido no parâmetro _ulFlags._ As informações existentes no objeto de destino que não são sobrescritas não são deixadas intocadas. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Você pode fornecer uma implementação completa de **CopyTo ou** contar com a implementação que o MAPI fornece em seu objeto de suporte. Se você quiser usar a implementação de MAPI, chame **IMAPISupport::D oCopyTo**. No entanto, se você delegar o processamento para **DoCopyTo** e passar o sinalizador MAPI_DECLINE_OK, evite a chamada de suporte e retorne MAPI_E_DECLINE_COPY vez. MAPI will call with this flag to avoid the possible recursion that can happen when folders are copied. 
  
Como a operação de cópia pode ser demorada, você deve exibir um indicador de progresso. Use a [implementação de IMAPIProgress](imapiprogressiunknown.md) passada no parâmetro  _lpProgress,_ se houver uma. Se  _lpProgress_ for **nulo,** chame o [método IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) para usar a implementação de MAPI. 
  
Não tente definir nenhuma propriedade conhecida somente leitura no objeto de destino; retornar MAPI_E_NO_ACCESS vez.
  
Os objetos de origem e destino devem usar as mesmas interfaces. Retornar MAPI_E_INVALID_PARAMETER se  _lpInterface_ não estiver definido. 
  
Retornar MAPI_E_INTERFACE_NOT_SUPPORTED se todas as interfaces conhecidas são excluídas.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Não definir o sinalizador MAPI_DECLINE_OK usuário; O MAPI o usa em suas chamadas para implementações **copyTo** do provedor de armazenamento de mensagens. 
  
Como as operações de copiar e mover podem demorar, você deve solicitar a exibição de um indicador de progresso definindo o sinalizador MAPI_DIALOG dados. You can set the  _lpProgress_ parameter to your implementation of **IMAPIProgress**, if you have one, or to **null**. Se  _lpProgress_ for **nulo,** **CopyTo** usará o indicador de progresso padrão que o MAPI fornece. 
  
Você pode suprimir a exibição de um indicador de progresso não definindo o MAPI_DIALOG sinalizador. **CopyTo** ignorará os  _parâmetros ulUIParam_ e  _lpProgress_ e não exibirá o indicador. 
  
 **CopyTo** pode relatar erros globais e individuais ou erros que ocorrem com uma ou mais propriedades. Esses erros individuais são colocados em uma **estrutura SPropProblemArray.** Você pode suprimir o relatório de erros no nível da propriedade passando **nulo**, em vez de um ponteiro válido, para o parâmetro de estrutura da matriz do problema de propriedade. 
  
Se você quiser receber informações sobre erros, passe um ponteiro de estrutura **SPropProblemArray** válido no parâmetro _lppProblems._ Quando **CopyTo** retornar S_OK, verifique se há possíveis erros com propriedades individuais na estrutura. Quando **CopyTo** retorna um erro, nenhuma informação é retornada na **estrutura SPropProblemArray.** Em vez disso, [chame IMAPIProp::GetLastError](imapiprop-getlasterror.md) para recuperar informações de erro detalhadas. 
  
Se **CopyTo** retornar S_OK, livre a estrutura **SPropProblemArray** retornada chamando a [função MAPIFreeBuffer.](mapifreebuffer.md) 
  
Se você copiar propriedades exclusivas do tipo de objeto de origem, deverá garantir que o objeto de destino seja do mesmo tipo. **CopyTo** não impede que você associe propriedades que normalmente pertencem a um tipo de objeto com outro tipo de objeto. Você pode copiar as propriedades que fazem sentido para o objeto de destino. Por exemplo, você não deve copiar as propriedades da mensagem para um contêiner do livro de endereços. 
  
Para garantir que você copie entre objetos do mesmo tipo, verifique se o objeto de origem e de destino são do mesmo tipo, comparando ponteiros de objeto ou chamando [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx). Definir o identificador de interface apontado por  _lpInterface_ para a interface padrão para o objeto de origem. Além disso, certifique-se de que o tipo de objeto **ou PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) seja o mesmo para os dois objetos. Por exemplo, se você copiar de uma mensagem, de definir  _lpInterface_ como IID_IMessage e o **PR_OBJECT_TYPE** para ambos os objetos MAPI_MESSAGE. 
  
Se um ponteiro inválido for passado no  _parâmetro lpDestObj,_ os resultados serão imprevisíveis. 
  
Excluir propriedades em uma **chamada CopyTo** pode ser útil. Por exemplo, alguns objetos têm propriedades específicas de uma única instância do objeto, como a data e a hora da entrega da mensagem. Para evitar copiar o tempo de entrega de uma mensagem quando você copiar a mensagem para uma pasta **diferente,** especifique PR_MESSAGE_DELIVERY_TIME ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)) na matriz de exclusão da marca de propriedade. Para excluir a lista de destinatários de uma mensagem, adicione a PR_MESSAGE_RECIPIENTS **(** [PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) à matriz de exclusão. Para excluir os anexos de uma mensagem, adicione a **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) à matriz.
  
Da mesma forma, impeça a cópia ou movimentação da hierarquia ou do conteúdo de um contêiner de pasta ou de um contêiner de address book incluindo **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) ou **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) na matriz de exclusão de marca de propriedade.
  
Para excluir propriedades da operação de movimentação ou cópia, inclua suas marcas de propriedade no _parâmetro lpExcludeProps._ Se você passar os resultados da macro **PROP_TAG** para criar uma marca de propriedade de um identificador específico na matriz de marca de propriedade, todas as propriedades com esse identificador serão excluídas. Por exemplo, a seguinte entrada na matriz de marca de propriedade faz com que todas as propriedades com um identificador de 0x8002 sejam excluídas, independentemente do tipo: 
  
 `PROP_TAG(PT_LONG, 0x8002)`
  
A **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) não pode ser incluída na _matriz lpExcludeProps._ 
  
A utilidade do recurso **CopyTo** para excluir interfaces talvez não seja tão óbvia quanto a utilidade da exclusão de propriedades. Você pode excluir uma interface ao copiar para um objeto que não tenha conhecimento de um grupo de propriedades. Por exemplo, se você copiar propriedades de uma pasta para um anexo, as únicas propriedades com as qual o anexo pode trabalhar são as propriedades genéricas disponíveis com qualquer [implementação IMAPIProp.](imapipropiunknown.md) Ao excluir [IMAPIFolder](imapifolderimapicontainer.md) da operação de cópia, o anexo não receberá nenhuma das propriedades de pasta mais específicas. 
  
Quando você usa o  _parâmetro rgiidExclude_ para excluir uma interface, ele também exclui todas as interfaces derivadas dessa interface. Por exemplo, excluir [IMAPIContainer](imapicontainerimapiprop.md) faz com que pastas ou contêineres de agendamento de endereço sejam excluídos, dependendo do tipo de provedor. Não **exclua IMAPIProp** [ou IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) porque muitas interfaces derivam delas. 
  
Ignore MAPI_E_COMPUTED erros retornados na estrutura **SPropProblemArray** no _parâmetro lppProblems._ 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadFromMSG  <br/> |MFCMAPI usa o método **IMAPIProp::CopyTo** para copiar propriedades de um arquivo .msg para um [objeto IMAPIMessageSite.](imapimessagesiteiunknown.md)  <br/> |
|FolderDlg.cpp  <br/> |CFolderDlg::HandlePaste  <br/> |MFCMAPI usa o método **IMAPIProp::CopyTo** para copiar propriedades de uma mensagem de origem para uma mensagem de destino durante uma operação de colar.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)
  
[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)
  
[IMAPISupport::DoCopyTo](imapisupport-docopyto.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriedade canônica PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[Propriedade canônica PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[Propriedade canônica PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)
  
[Propriedade canônica PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)
  
[Propriedade canônica PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[Propriedade canônica PidTagObjectType](pidtagobjecttype-canonical-property.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

