---
title: IMAPIPropGetIDsFromNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetIDsFromNames
api_type:
- COM
ms.assetid: e3f501a4-a8ee-43d7-bd83-c94e7980c398
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 28880b818bc80e31cae0c695d4aac92eb9555cac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314837"
---
# <a name="imapipropgetidsfromnames"></a>IMAPIProp::GetIDsFromNames

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece os identificadores de propriedade que correspondem a um ou mais nomes de propriedade.
  
```cpp
HRESULT GetIDsFromNames(
  ULONG cPropNames,
  LPMAPINAMEID FAR * lppPropNames,
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTags
);
```

## <a name="parameters"></a>Parâmetros

 _cPropNames_
  
> no A contagem de nomes de propriedade apontados pelo parâmetro _lppPropNames_ . Se _lppPropNames_ for nulo, o parâmetro _cPropNames_ deverá ser 0. 
    
 _lppPropNames_
  
> no Um ponteiro para uma matriz de nomes de propriedade ou nulo. Passando identificadores de propriedade de solicitações nulos para todos os nomes de propriedade em todos os conjuntos de propriedades sobre os quais o objeto tem informações. O parâmetro _lppPropNames_ não deve ser nulo se o sinalizador MAPI_CREATE estiver definido no parâmetro _parâmetroulflags_ . 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que indica como os identificadores de propriedade devem ser retornados. O seguinte sinalizador pode ser definido:
    
MAPI_CREATE 
  
> Atribui um identificador de propriedade, se ainda não tiver sido atribuído um ou mais dos nomes incluídos na matriz de nomes de propriedade apontada por _lppPropNames_. Este sinalizador registra internamente o identificador na tabela de mapeamento de nome para identificador.
    
 _lppPropTags_
  
> bota Um ponteiro para um ponteiro para uma matriz de marcas de propriedade que contém identificadores de propriedade recém-criados ou existentes. Os tipos de propriedade para as marcas de propriedade nesta matriz são definidos como **PT_UNSPECIFIED**.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Os identificadores para os nomes das propriedades especificadas foram retornados com êxito.
    
MAPI_E_NO_SUPPORT 
  
> O objeto não dá suporte a propriedades nomeadas.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> Memória inSuficiente disponível para recuperar os identificadores.
    
MAPI_E_TOO_BIG 
  
> A operação não pode ser executada porque requer muitas marcas de propriedade a serem retornadas.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada teve êxito geral, mas não foi possível retornar um ou mais identificadores de propriedade. O tipo de propriedade correspondente para cada propriedade indisponível é definido como **PT_ERROR** e seu identificador como zero. Quando esse aviso for retornado, manipule a chamada como bem-sucedida. Para testar esse aviso, use a macro **HR_FAILED** . Consulte [usando macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPIProp:: GetIDsFromNames** recupera uma matriz de marcas de propriedade que mantêm os identificadores de propriedade para uma ou mais propriedades nomeadas. **IMAPIProp:: GetIDsFromNames** pode ser chamado para fazer o seguinte: 
  
- Criar identificadores para novos nomes.
    
- Recuperar identificadores para nomes específicos.
    
- Recuperar identificadores de todas as propriedades nomeadas incluídas no mapeamento do objeto.
    
Propriedades nomeadas normalmente são usadas por provedores de repositórios de mensagens para pastas e mensagens. Outros objetos, como usuários de mensagens e seções de perfil, podem não oferecer suporte à associação de nomes aos identificadores de propriedade e podem retornar MAPI_E_NO_SUPPORT de **GetIDsFromNames**.
  
Se houver um erro que retorne um identificador para um nome específico, **GetIDsFromNames** retornará MAPI_W_ERRORS_RETURNED e definirá o tipo de propriedade na entrada de matriz da marca de propriedade que corresponde ao nome como **PT_ERROR** e o identificador como zero. 
  
O mapeamento de nome para identificador é representado pela propriedade **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) de um objeto. **PR_MAPPING_SIGNATURE** contém uma estrutura [MAPIUID](mapiuid.md) que indica o provedor de serviços responsável pelo objeto. Se a propriedade **PR_MAPPING_SIGNATURE** for a mesma de dois objetos, suponha que esses objetos usem o mesmo mapeamento de nome para identificador. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Os identificadores que você passa de volta na matriz de marca de propriedade apontada pelo parâmetro _lppPropNames_ devem estar no intervalo 0X8000 para 0xFFFE. As entradas nessa matriz devem estar na mesma ordem que os nomes passados na matriz de nomes de propriedade apontada por _lppPropNames_. 
  
Se você oferecer suporte a propriedades nomeadas em um contêiner, use o mesmo mapeamento de nome para todos os objetos em seu contêiner (ou seja, não use um mapeamento diferente para cada pasta em seu repositório de mensagens ou cada mensagem em sua pasta).
  
## <a name="notes-to-callers"></a>Notas para chamadores

Como os tipos de propriedade para os identificadores retornados na matriz de marca de propriedade apontada por _lppPropTags_ estão definidos como **PT_UNSPECIFIED**, você precisará chamar o método [IMAPIProp::](imapiprop-setprops.md) SetProps para recuperar os tipos precisos. 
  
Se você mover ou copiar objetos com propriedades nomeadas e os objetos de origem e de destino tiverem diferentes assinaturas de mapeamento conforme indicado pelos valores das suas propriedades **PR_MAPPING_SIGNATURE** , você deve preservar os nomes durante essas operações. Para preservar os nomes de propriedade, ajuste os identificadores de propriedade correspondentes para corresponder ao mapeamento de nome para identificador do objeto de destino. 
  
Alguns objetos têm um limite quanto ao número de identificadores de propriedade que podem ser nomeados. Se uma chamada para **GetIDsFromNames** fizer com que esse limite seja excedido, o método retornará MAPI_E_TOO_BIG. Nesse caso, consulte por identificador. 
  
Para obter mais informações, consulte [MAPI Named Properties](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl. cpp  <br/> |CSingleMAPIPropListCtrl:: FindAllNamedPropsUsed  <br/> |MFCMAPI usa o método **IMAPIProp:: GetIDsFromNames** para obter as marcas de propriedade de todas as propriedades nomeadas que foram mapeadas.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[MAPINAMEID](mapinameid.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[MAPI denominada propriedades](mapi-named-properties.md)
  
[Usando macros para tratamento de erros](using-macros-for-error-handling.md)

