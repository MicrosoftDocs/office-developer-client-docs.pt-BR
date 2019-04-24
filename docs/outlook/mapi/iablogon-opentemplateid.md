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
  
Abre uma entrada de destinatário que tem dados residindo em um provedor de catálogo de endereços de host.
  
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
  
> no A contagem de bytes no identificador de modelo apontado pelo parâmetro _lpTemplateID_ . 
    
 _lpTemplateID_
  
> no Um ponteiro para o identificador de modelo ou a propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) da entrada de destinatário a ser aberta.
    
 _ulTemplateFlags_
  
> no Uma bitmask de sinalizadores usados para indicar como abrir a entrada representada pelo identificador de modelo. O seguinte sinalizador pode ser definido:
    
FILL_ENTRY 
  
> O provedor de host está criando uma nova entrada em seu contêiner com base na entrada representada pelo identificador de modelo. O método **IABLogon:: OpenTemplateID** deve executar uma inicialização específica da entrada do provedor de host usando a implementação [IMAPIProp: IUnknown](imapipropiunknown.md) no parâmetro _lpMAPIPropData_ ou retornar um **IMAPIProp personalizado **implementação de interface no parâmetro _lppMAPIPropNew_ . 
    
 _lpMAPIPropData_
  
> no Um ponteiro para o objeto Property do provedor de host e a implementação de uma interface derivada de **IMAPIProp**.
    
 _lpInterface_
  
> no Um ponteiro para o identificador de interface (IID) que representa o tipo de ponteiro de interface a ser retornado no parâmetro _lppMAPIPropNew_ . Passar **nulo** retorna a interface de usuário de mensagens padrão, [IMailUser: IMAPIProp](imailuserimapiprop.md).
    
 _lppMAPIPropNew_
  
> bota Um ponteiro para o objeto Property associado e uma implementação de uma interface derivada de **IMAPIProp**.
    
 _lpMAPIPropSibling_
  
> bota Serve deve ser **nulo**.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O código apropriado foi vinculado com êxito a dados relacionados no provedor de host.
    
MAPI_E_NO_SUPPORT 
  
> O objeto não oferece suporte a IDs de modelo.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O identificador de modelo passado no parâmetro _lpTemplateID_ não é reconhecido pelo provedor de catálogo de endereços. 
    
## <a name="remarks"></a>Comentários

O método **IABLogon:: OpenTemplateID** é implementado apenas por provedores de catálogo de endereços que precisam manter controle sobre cópias de suas entradas localizadas nos contêineres de provedores de host. Os provedores que implementam o **OpenTemplateID** são conhecidos como provedores de catálogos de endereços externos. Os provedores de host chamam [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) para criar uma entrada copiada ou abrir a entrada copiada, e o MAPI passa na chamada para **IABLogon:: OpenTemplateID**. **IABLogon:: OpenTemplateID** abre a entrada e vincula o código que o controla aos dados no provedor de host. 
  
Em vez de usar um identificador de entrada, **IABLogon:: OpenTemplateID** usa outra propriedade, o identificador de modelo de entrada, **PR_TEMPLATEID**. Os identificadores de modelo devem ser suportados para entradas cujo código deve estar vinculado aos dados de um provedor de host.
  
Alguns exemplos de quando um provedor de catálogo de endereços deve implementar **IABLogon:: OpenTemplateID** são os seguintes: 
  
- Para atualizar periodicamente os dados de uma entrada copiada de modo que ela permaneça sincronizada com o original.
    
- Para implementar a funcionalidade que o provedor de host não pode implementar, como preencher dinamicamente uma lista que aparece na tabela de detalhes da entrada de dados em um servidor.
    
- Para controlar a interação entre as propriedades na entrada do provedor de host e a entrada original, como computação do **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) dos valores dos controles de edição na exibição de detalhes que contêm diferentes componentes do endereço.
    
## <a name="notes-to-implementers"></a>Observações para implementadores

Quando um provedor de host copia ou cria uma entrada de seu provedor e você fornece uma implementação de objeto Property por meio de **IABLogon:: OpenTemplateID**, você lida com a maioria das chamadas para manter a entrada. No enTanto, como o provedor de host para encaminhar essas chamadas para você, o provedor de host pode interceptar qualquer chamada e executar o processamento personalizado antes de encaminhar a chamada.
  
Você deve usar as seguintes diretrizes em suas implementações de objeto de propriedade:
  
- Quando [IMAPIProp::](imapiprop-getprops.md) GetProps é chamado, determina se a solicitação é para uma propriedade calculada e, se for, manipulá-la. Transferir todas as solicitações de propriedades não computadas para o provedor de host. 
    
- Quando [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) é chamado para abrir qualquer tabela, exceto a tabela de exibição de detalhes, para lidar com a solicitação. A maioria das tabelas não pode ser copiada com precisão para o provedor de host. Você deve gerar a **** implementação IMAPITable para essas tabelas solicitadas. A propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) da tabela de detalhes deve ser copiada para o provedor de host. Isso permite que este provedor gere a tabela localmente. Você pode querer encapsular a implementação da tabela de exibição para gerar notificações de exibição de tabela. 
    
- Quando [IMAPIProp::](imapiprop-setprops.md) SetProps é chamado, o provedor de host pode validar os dados antes de permitir que você defina as propriedades. Você pode verificar se todas as propriedades necessárias foram definidas ou computadas. Se um erro for detectado, retorne o valor de erro apropriado e, se possível, qualquer explicação adicional por meio de [IMAPIProp:: GetLastError](imapiprop-getlasterror.md).
    
- Quando [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) é chamado, o provedor de host pode querer executar o processamento antes de salvar a entrada. Você deve salvar todos os dados afetados pelas propriedades alteradas, como um novo endereço, na entrada do provedor de host. 
    
Em geral, faça sua implementação da entrada que você passa de volta para o provedor de host interceptar todos os métodos para executar a manipulação específica de contexto das propriedades relevantes. Se o sinalizador FILL_ENTRY for passado no parâmetro _ulTemplateFlags_ , defina todas as propriedades para a entrada. 
  
Se você retornar um novo objeto Property no parâmetro _lppMAPIPropNew_ , chame o método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) do objeto Property do provedor de host para manter uma referência. Todas as chamadas por meio do objeto acoplado que a implementação de **IMAPIProp** retornada no _lppMAPIPropNew_ devem ser roteadas para o método correspondente no objeto de propriedade de host depois de serem lidas pelo objeto acoplado. 
  
Os identificadores de propriedade de quaisquer propriedades nomeadas que são passadas pelo seu objeto Property associado estão no namespace do identificador do provedor. Sua implementação do método [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) deve determinar os nomes das propriedades para que ele possa executar qualquer tarefa específica do modelo. Da mesma forma, as propriedades que seu provedor passa para o provedor de host também devem estar no namespace. Por exemplo, se você definir uma propriedade nomeada no **OpenTemplateID**, deverá usar um de seus identificadores para o nome — criando-o, se necessário, chamando o método [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) . 
  
Se você não reconhece o identificador de entrada passado no _lpTemplateID_, retorne MAPI_E_UNKNOWN_ENTRYID.
  
Para obter mais informações sobre como trabalhar com identificadores de modelo de catálogo de endereços, consulte [atuando como um provedor de catálogo de endereços externo](acting-as-a-foreign-address-book-provider.md).
  
## <a name="see-also"></a>Confira também



[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[Propriedade canônica PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

