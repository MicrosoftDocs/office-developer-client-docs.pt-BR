---
title: IABLogonOpenTemplateID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenTemplateID
api_type:
- COM
ms.assetid: 751c36d3-c39e-4357-a60a-88685a378de0
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bc68878a25873533162df7e1671e483c3bb77865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334745"
---
# <a name="iablogonopentemplateid"></a>IABLogon::OpenTemplateID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma entrada de destinatário que tem dados residindo em um provedor de agendamento de endereço de host.
  
```cpp
HRESULT OpenTemplateID(
  ULONG cbTemplateID,
  LPENTRYID lpTemplateID,
  ULONG ulTemplateFlags,
  LPMAPIPROP lpMAPIPropData,
  LPCIID lpInterface,
  LPMAPIPROP FAR * lppMAPIPropNew,
  LPMAPIPROP lpMAPIPropSibling
);
```

## <a name="parameters"></a>Parâmetros

 _cbTemplateID_
  
> [in] A contagem de byte no identificador de modelo apontado pelo parâmetro _lpTemplateID._ 
    
 _lpTemplateID_
  
> [in] Um ponteiro para o identificador de modelo ou **PR_TEMPLATEID** propriedade ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) da entrada do destinatário a ser aberta.
    
 _ulTemplateFlags_
  
> [in] Uma bitmask de sinalizadores usada para indicar como abrir a entrada representada pelo identificador de modelo. O sinalizador a seguir pode ser definido:
    
FILL_ENTRY 
  
> O provedor de host está criando uma nova entrada em seu contêiner com base na entrada representada pelo identificador do modelo. O método **IABLogon::OpenTemplateID** deve executar a inicialização específica da entrada do provedor host usando a implementação [IMAPIProp : IUnknown](imapipropiunknown.md) no parâmetro _lpMAPIPropData_ ou retornar uma implementação de interface **IMAPIProp** personalizada no parâmetro _lppMAPIPropNew._ 
    
 _lpMAPIPropData_
  
> [in] Um ponteiro para o objeto de propriedade do provedor de host e implementação de uma interface derivada de **IMAPIProp**.
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador da interface (IID) que representa o tipo de ponteiro da interface a ser retornado no parâmetro _lppMAPIPropNew._ Passar **nulo** retorna a interface do usuário padrão de mensagens, [IMailUser : IMAPIProp](imailuserimapiprop.md).
    
 _lppMAPIPropNew_
  
> [out] Um ponteiro para o objeto de propriedade vinculada e uma implementação de uma interface derivada de **IMAPIProp**.
    
 _lpMAPIPropSibling_
  
> [out] Reservado; deve ser **nulo**.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O código apropriado foi vinculado com êxito aos dados relacionados no provedor de host.
    
MAPI_E_NO_SUPPORT 
  
> O objeto não dá suporte a IDs de modelo.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O identificador de modelo passado no  _parâmetro lpTemplateID_ não é reconhecido pelo provedor do address book. 
    
## <a name="remarks"></a>Comentários

O **método IABLogon::OpenTemplateID** é implementado apenas por provedores de agendamento de endereço que precisam manter o controle sobre cópias de suas entradas localizadas nos contêineres de provedores de host. Provedores que implementam **OpenTemplateID são** conhecidos como provedores de livro de endereços externos. Provedores de host chamam [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para criar uma entrada copiada ou abrir a entrada copiada, e MAPI passa a chamada para **IABLogon::OpenTemplateID**. **IABLogon::OpenTemplateID** abre a entrada e vincula o código que a controla aos dados no provedor de host. 
  
Em vez de usar um identificador de entrada, **IABLogon::OpenTemplateID** usa outra propriedade, o identificador de modelo da entrada, **PR_TEMPLATEID**. Os identificadores de modelo devem ter suporte para entradas cujo código deve ser vinculado aos dados em um provedor de host.
  
Alguns exemplos de quando um provedor de agendamento de endereços deve implementar **IABLogon::OpenTemplateID** são: 
  
- Para atualizar periodicamente os dados de uma entrada copiada para que permaneçam sincronizados com o original.
    
- Para implementar a funcionalidade que o provedor de host não pode implementar, como preencher dinamicamente uma lista que aparece na tabela de detalhes da entrada de dados em um servidor.
    
- Para controlar a interação entre as propriedades na entrada do provedor host e a entrada original, como calcular o **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) dos valores dos controles de edição na exibição de detalhes que contêm diferentes componentes do endereço.
    
## <a name="notes-to-implementers"></a>Observações para implementadores

Quando um provedor de host copia ou cria uma entrada de seu provedor e você fornece uma implementação de objeto de propriedade por meio de **IABLogon::OpenTemplateID**, você lida com a maioria das chamadas para manter a entrada. No entanto, como o provedor de host deve encaminhar essas chamadas para você, o provedor de host pode interceptar qualquer chamada e executar o processamento personalizado antes de encaminhar a chamada.
  
Você deve usar as seguintes diretrizes em suas implementações de objeto de propriedade:
  
- Quando [IMAPIProp::GetProps](imapiprop-getprops.md) for chamado, determine se a solicitação é para uma propriedade computada e, se for, lidar com ela. Transfira todas as solicitações de propriedades nãocomputadas para o provedor de host. 
    
- Quando [IMAPIProp::OpenProperty](imapiprop-openproperty.md) é chamado para abrir qualquer tabela, exceto a tabela de exibição de detalhes, manipular a solicitação. A maioria das tabelas não pode ser copiada com precisão para o provedor de host. Você deve gerar a **implementação IMAPITable** para essas tabelas solicitadas. A tabela de **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) deve ser copiada para o provedor de host. Isso permite que esse provedor gere a tabela localmente. Talvez você queira quebrar a implementação da tabela de exibição para gerar notificações de tabela de exibição. 
    
- Quando [IMAPIProp::SetProps](imapiprop-setprops.md) é chamado, o provedor de host pode validar os dados antes de permitir a definição das propriedades. Você pode verificar se todas as propriedades necessárias foram definidas ou computadas. Se um erro for detectado, retorne o valor de erro apropriado e, se possível, qualquer explicação adicional por meio de [IMAPIProp::GetLastError](imapiprop-getlasterror.md).
    
- Quando [IMAPIProp::SaveChanges](imapiprop-savechanges.md) é chamado, o provedor host pode querer executar o processamento antes de salvar a entrada. Você deve salvar quaisquer dados afetados pelas propriedades alteradas, como um novo endereço, na entrada do provedor de host. 
    
Em geral, faça sua implementação da entrada que você passa de volta para o provedor host interceptar todos os métodos para executar manipulação específica de contexto das propriedades relevantes. Se o FILL_ENTRY sinalizador for passado no  _parâmetro ulTemplateFlags,_ defina todas as propriedades para a entrada. 
  
Se você retornar um novo objeto de propriedade no parâmetro  _lppMAPIPropNew,_ chame o método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) do objeto de propriedade do provedor de host para manter uma referência. Todas as chamadas através do objeto vinculado que a implementação **de IMAPIProp** retornada em  _lppMAPIPropNew_ devem ser roteadas para o método correspondente no objeto de propriedade host depois que eles são tratados pelo objeto vinculado. 
  
Os identificadores de propriedade de quaisquer propriedades nomeadas que são passadas pelo objeto de propriedade vinculada estão no namespace do identificador do provedor. Sua implementação do [método IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) deve determinar os nomes das propriedades para que ele possa executar qualquer tarefa específica do modelo. Da mesma forma, as propriedades que seu provedor passa para o provedor de host também devem estar em seu namespace. Por exemplo, se você definir uma propriedade nomeada em **OpenTemplateID**, deverá usar um de seus identificadores para o nome criando-a, se necessário, chamando o método [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) 
  
Se você não reconhecer o identificador de entrada passado  _em lpTemplateID,_ retorne MAPI_E_UNKNOWN_ENTRYID.
  
For more information about how to work with address book template identifiers, see [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).
  
## <a name="see-also"></a>Confira também



[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[Propriedade canônica PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

