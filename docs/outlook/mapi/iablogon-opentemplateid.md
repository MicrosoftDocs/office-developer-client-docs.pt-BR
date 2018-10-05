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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: bc68878a25873533162df7e1671e483c3bb77865
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384630"
---
# <a name="iablogonopentemplateid"></a>IABLogon::OpenTemplateID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma entrada do destinatário que possui dados que residem em um provedor de catálogo de endereço de host.
  
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
  
> [in] A contagem de bytes do identificador de modelo apontado pelo parâmetro _lpTemplateID_ . 
    
 _lpTemplateID_
  
> [in] Um ponteiro para o identificador de modelo, ou a propriedade de **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)), da entrada do destinatário a serem abertas.
    
 _ulTemplateFlags_
  
> [in] Uma bitmask dos sinalizadores usados para indicar como abrir a entrada representada pelo identificador de modelo. O seguinte sinalizador pode ser definido:
    
FILL_ENTRY 
  
> O provedor de host está criando uma nova entrada no seu contêiner com base na entrada representada pelo identificador de modelo. O método **IABLogon:: OpenTemplateID** deve executar inicialização específica da entrada do provedor de host usando o [IMAPIProp: IUnknown](imapipropiunknown.md) implementação no parâmetro _lpMAPIPropData_ ou retorno um sinalizador **IMAPIProp **implementação no parâmetro _lppMAPIPropNew_ de interface. 
    
 _lpMAPIPropData_
  
> [in] Um ponteiro para o objeto de propriedade e a implementação de uma interface do provedor de host é derivado do **IMAPIProp**.
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa o tipo de ponteiro de interface a ser retornado no parâmetro _lppMAPIPropNew_ . Passar **Nulo** retorna o padrão de mensagens de interface do usuário, [IMailUser: IMAPIProp](imailuserimapiprop.md).
    
 _lppMAPIPropNew_
  
> [out] Um ponteiro para o objeto de propriedade acoplada e uma implementação de uma interface derivada **IMAPIProp**.
    
 _lpMAPIPropSibling_
  
> [out] Reservado; deve ser **nula**.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O código apropriado com êxito estava vinculado a dados relacionados no provedor de host.
    
MAPI_E_NO_SUPPORT 
  
> O objeto não suporta as IDs de modelo.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O identificador de modelo passado no parâmetro _lpTemplateID_ não é reconhecido pelo provedor de catálogo de endereços. 
    
## <a name="remarks"></a>Comentários

O método **IABLogon:: OpenTemplateID** é implementado apenas por provedores de catálogo de endereços que precisam manter o controle sobre cópias de suas entradas que estão localizadas em contêineres de provedores de host. Os provedores que implementam **OpenTemplateID** são conhecidos como provedores de catálogo de endereço estrangeiro. Ligue para provedores de host [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para criar uma entrada copiada ou abra a entrada copiada e MAPI passa na chamada **IABLogon:: OpenTemplateID**. **IABLogon:: OpenTemplateID** abre a entrada e vincula o código que controla-lo aos dados no provedor de host. 
  
Em vez de usar um identificador de entrada, **IABLogon:: OpenTemplateID** usa a propriedade outra, identificador de modelo da entrada, **PR_TEMPLATEID**. Identificadores de modelo devem ser suportados para entradas cujo código deve ser vinculado a dados em um provedor de host.
  
Alguns exemplos de quando um provedor de catálogo de endereços deverá implementar **IABLogon:: OpenTemplateID** são os seguintes: 
  
- Para atualizar periodicamente os dados de uma entrada copiada para que ele fique sincronizado com o original.
    
- Para implementar a funcionalidade que não é possível implementar o provedor de host, como popular dinamicamente uma lista que aparece na tabela de detalhes da entrada de dados em um servidor.
    
- Para controlar a interação entre as propriedades na entrada do provedor de host e a entrada original, como o **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) dos valores de controles de edição na exibição detalhes que contêm diferentes de computação componentes do endereço.
    
## <a name="notes-to-implementers"></a>Observações para implementadores

Quando um provedor de host copia ou cria uma entrada do seu provedor e o fornecimento de uma implementação do objeto de propriedade por meio de **IABLogon:: OpenTemplateID**, você pode manipular a maioria das chamadas para manter a entrada. No entanto, porque ele é o provedor de host para encaminhar essas chamadas para você, o provedor de host pode interceptar qualquer chamada e realizar processamento personalizado antes de encaminhar a chamada.
  
Você deve usar as seguintes diretrizes em suas implementações de objeto de propriedade:
  
- Quando [IMAPIProp::GetProps](imapiprop-getprops.md) é chamado, determine se a solicitação for para uma propriedade calculada e, se for, manipulá-lo. Transferi todas as solicitações para propriedades noncomputed para o provedor de host. 
    
- Quando [IMAPIProp::OpenProperty](imapiprop-openproperty.md) é chamado para abrir qualquer tabela exceto os detalhes de exibição tabela, processar a solicitação. A maioria das tabelas não pode ser copiado para o provedor de host com precisão. É necessário gerar a implementação de **IMAPITable** para nestas tabelas solicitadas. A propriedade de **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) da tabela de detalhes deve ser copiada para o provedor de host. Isso permite que esse provedor gerar a tabela localmente. Talvez você queira quebrar a implementação da tabela de exibição para gerar notificações de tabela de exibição. 
    
- Quando [IMAPIProp::SetProps](imapiprop-setprops.md) é chamado, o provedor de host possa validar os dados antes de permitir que você defina as propriedades. Você pode verificar que todas as propriedades necessárias foram definidas ou computadas. Se for detectado um erro, retorne o valor de erro apropriado e, se possível, qualquer explicação adicional por meio de [IMAPIProp::GetLastError](imapiprop-getlasterror.md).
    
- Quando [IMAPIProp::SaveChanges](imapiprop-savechanges.md) é chamado, o provedor de host pode ser executada antes de salvar a entrada de processamento. Você deve salvar todos os dados afetados por propriedades alteradas, como um novo endereço na entrada do provedor de host. 
    
Em geral, verifique a implementação da entrada que você passa de volta para o provedor de host interceptar todos os métodos para executar a manipulação de contexto específicos das propriedades relevantes. Se o sinalizador FILL_ENTRY é passado no parâmetro _ulTemplateFlags_ , defina todas as propriedades para a entrada. 
  
Se você retornar um novo objeto property no parâmetro _lppMAPIPropNew_ , chame o método [AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) do objeto de propriedade do provedor de host para manter uma referência. Todas as chamadas através do objeto acoplado que a implementação de **IMAPIProp** retornada em _lppMAPIPropNew_ devem ser roteadas para seus métodos correspondentes do objeto de propriedade de host depois que eles são tratados pelo objeto acoplado. 
  
Os identificadores de propriedade de todas as propriedades nomeadas que são passadas para seu objeto de propriedade acoplada estão no namespace de identificador do seu provedor. A implementação do método [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) deve determinar os nomes das propriedades para que ele possa realizar todas as tarefas específicas do modelo. Da mesma forma, as propriedades que seu provedor passa ao provedor de host também devem ser em seu namespace. Por exemplo, se você definir uma propriedade nomeada no **OpenTemplateID**, você deve usar um dos seus identificadores para o nome — criá-la, se necessário, chamando o método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . 
  
Se você não reconhecer o identificador de entrada passado _lpTemplateID_, retorne MAPI_E_UNKNOWN_ENTRYID.
  
Para obter mais informações sobre como trabalhar com identificadores de modelo de catálogo de endereços, consulte [atuando como um provedor de catálogo de endereços estrangeira](acting-as-a-foreign-address-book-provider.md).
  
## <a name="see-also"></a>Confira também



[IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)
  
[Propriedade canônica PidTagTemplateid](pidtagtemplateid-canonical-property.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

