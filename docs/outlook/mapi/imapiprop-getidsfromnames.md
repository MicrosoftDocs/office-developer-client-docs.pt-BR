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
ms.openlocfilehash: 5247ca71c88b9c0f8591a732746a17204265741c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767152"
---
# <a name="imapipropgetidsfromnames"></a>IMAPIProp::GetIDsFromNames

  
  
**Aplica-se a**: Outlook 
  
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
  
> [in] A contagem de nomes de propriedade apontado pelo parâmetro _lppPropNames_ . Se _lppPropNames_ for NULL, o parâmetro _cPropNames_ deve ser 0. 
    
 _lppPropNames_
  
> [in] Um ponteiro para uma matriz de nomes de propriedade ou nulo. Identificadores de propriedade para todos os nomes de propriedade em todos os conjuntos de propriedade sobre quais o objeto possui informações de solicitações de passagem nula. O parâmetro _lppPropNames_ não deve ser NULL se o sinalizador MAPI_CREATE é definido no parâmetro _ulFlags_ . 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que indica como os identificadores de propriedade devem ser retornados. O seguinte sinalizador pode ser definido:
    
MAPI_CREATE 
  
> Atribui um identificador de propriedade, se um tem ainda não foram atribuído, a um ou mais dos nomes incluídos na matriz de nome de propriedade apontado pela _lppPropNames_. Esse sinalizador internamente registra o identificador na tabela de mapeamento de identificador do nome.
    
 _lppPropTags_
  
> [out] Um ponteiro para um ponteiro para uma matriz de marcas de propriedade que contém os identificadores de propriedade existente ou recentemente atribuído. Os tipos de propriedade para as marcas de propriedade nessa matriz são definidos com **PT_UNSPECIFIED**.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Os identificadores para os nomes de propriedade especificado foram retornados com êxito.
    
MAPI_E_NO_SUPPORT 
  
> O objeto não dá suporte a propriedades nomeadas.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> Memória insuficiente estava disponível para recuperar os identificadores.
    
MAPI_E_TOO_BIG 
  
> A operação não pode ser executada porque requer muitas marcas de propriedade a ser retornado.
    
MAPI_W_ERRORS_RETURNED 
  
> Chamada bem-sucedida, mas um ou mais identificadores de propriedade não puderam ser retornados. O tipo de propriedade correspondentes para cada propriedade indisponível é definido para **PT_ERROR** e seu identificador como zero. Quando esse aviso é retornado, lidar com a chamada como bem sucedida. Para testar esse aviso, use a macro **HR_FAILED** . Consulte [usando Macros para tratamento de erros](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Comentários

O método **IMAPIProp::GetIDsFromNames** recupera uma matriz de marcas de propriedade que armazenam os identificadores de propriedade para um ou mais propriedades nomeadas. **IMAPIProp::GetIDsFromNames** pode ser chamado para fazer o seguinte: 
  
- Crie identificadores para novos nomes.
    
- Recupere os identificadores para nomes específicos.
    
- Recupere os identificadores para todas as propriedades nomeadas que estão incluídos no mapeamento do objeto.
    
Propriedades nomeadas geralmente são usadas por provedores de repositório de mensagem para mensagens e pastas. Outros objetos, como mensagens de seções de perfil e os usuários podem não suportar a associação de nomes aos identificadores de propriedade e podem retornar MAPI_E_NO_SUPPORT da **GetIDsFromNames**.
  
Se houver um erro dizendo que retorna um identificador para um determinado nome, **GetIDsFromNames** retorna MAPI_W_ERRORS_RETURNED e define o tipo de propriedade a entrada de matriz de marca de propriedade que corresponde ao nome **PT_ERROR** e o identificador como zero. 
  
Mapeamento de identificador do nome é representado pela propriedade de **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) de um objeto. **PR_MAPPING_SIGNATURE** contém uma estrutura [MAPIUID](mapiuid.md) que indica o provedor de serviços responsável pelo objeto. Se a propriedade **PR_MAPPING_SIGNATURE** é o mesmo para dois objetos, suponha que esses objetos usam o mesmo mapeamento de identificador do nome. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Os identificadores que você passa de volta na propriedade tag matriz apontado pelo parâmetro _lppPropNames_ devem estar no intervalo 0x8000 para 0xFFFE. As entradas nessa matriz devem estar na mesma ordem em que os nomes passado na matriz de nome de propriedade apontadas pela _lppPropNames_. 
  
Caso você ofereça suporte a propriedades nomeadas em um recipiente, use o mesmo mapeamento de identificador do nome para todos os objetos em seu contêiner (ou seja, não use um mapeamento diferente para cada pasta no seu armazenamento de mensagens ou de cada mensagem na pasta).
  
## <a name="notes-to-callers"></a>Notas para chamadores

Como os tipos de propriedade para os identificadores retornados na matriz de marca de propriedade apontado pela _lppPropTags_ estiver definidos como **PT_UNSPECIFIED**, você terá que chamar o método [IMAPIProp::SetProps](imapiprop-setprops.md) para recuperar os tipos exatos. 
  
Se você move ou copiar objetos com propriedades nomeadas e os objetos de origem e destino têm assinaturas de mapeamento diferente como indicado pela lista os valores das suas propriedades **PR_MAPPING_SIGNATURE** , os nomes devem ser preservadas durante essas operações. Para preservar os nomes de propriedade, ajuste os identificadores de propriedade correspondentes para coincidir com o mapeamento de identificador do nome do objeto de destino. 
  
Alguns objetos tem um limite como para o número de identificadores de propriedade, que eles podem name. Se uma chamada para **GetIDsFromNames** faz exceder esse limite, o método retornará MAPI_E_TOO_BIG. Nesse caso, a consulta por identificador. 
  
Para obter mais informações, consulte [Propriedades de chamada de MAPI](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedPropsUsed  <br/> |MFCMAPI usa o método **IMAPIProp::GetIDsFromNames** para obter as marcas de propriedade para todas as propriedades nomeadas que foram mapeadas.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[MAPINAMEID](mapinameid.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[MAPI denominada propriedades](mapi-named-properties.md)
  
[Usar macros para lidar com erros](using-macros-for-error-handling.md)

