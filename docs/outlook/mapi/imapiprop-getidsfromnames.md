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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433581"
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
  
> [in] A contagem de nomes de propriedade apontados pelo _parâmetro lppPropNames._ Se  _lppPropNames_ for NULL, o  _parâmetro cPropNames_ deverá ser 0. 
    
 _lppPropNames_
  
> [in] Um ponteiro para uma matriz de nomes de propriedade ou NULL. Passar identificadores de propriedade de solicitações NULL para todos os nomes de propriedade em todos os conjuntos de propriedades sobre os quais o objeto tem informações. O _parâmetro lppPropNames_ não deve ser NULL se o sinalizador MAPI_CREATE estiver definido no _parâmetro ulFlags._ 
    
 _ulFlags_
  
> [in] Uma bitmask de sinalizadores que indica como os identificadores de propriedade devem ser retornados. O sinalizador a seguir pode ser definido:
    
MAPI_CREATE 
  
> Atribui um identificador de propriedade, se um ainda não tiver sido atribuído, a um ou mais dos nomes incluídos na matriz de nomes de propriedade apontados por  _lppPropNames_. Esse sinalizador registra internamente o identificador na tabela de mapeamento de nome para identificador.
    
 _lppPropTags_
  
> [out] Um ponteiro para um ponteiro para uma matriz de marcas de propriedade que contém identificadores de propriedade existentes ou atribuídos recentemente. Os tipos de propriedade para as marcas de propriedade nesta matriz são definidos **como PT_UNSPECIFIED**.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Os identificadores dos nomes de propriedade especificados foram retornados com êxito.
    
MAPI_E_NO_SUPPORT 
  
> O objeto não dá suporte a propriedades nomeadas.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> Memória insuficiente disponível para recuperar os identificadores.
    
MAPI_E_TOO_BIG 
  
> A operação não pode ser executada porque exige muitas marcas de propriedade para serem retornadas.
    
MAPI_W_ERRORS_RETURNED 
  
> A chamada foi bem-sucedida em geral, mas um ou mais identificadores de propriedade não puderam ser retornados. O tipo de propriedade correspondente para cada propriedade indisponível é **definido como PT_ERROR** e seu identificador como zero. Quando esse aviso for retornado, tratar a chamada como bem-sucedida. Para testar esse aviso, use a **HR_FAILED** macro. Consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Comentários

O **método IMAPIProp::GetIDsFromNames** recupera uma matriz de marcas de propriedade que mantém os identificadores de propriedade para uma ou mais propriedades nomeadas. **IMAPIProp::GetIDsFromNames** pode ser chamado para fazer o seguinte: 
  
- Crie identificadores para novos nomes.
    
- Recuperar identificadores para nomes específicos.
    
- Recupere identificadores de todas as propriedades nomeadas incluídas no mapeamento do objeto.
    
Propriedades nomeadas são normalmente usadas por provedores de armazenamento de mensagens para pastas e mensagens. Outros objetos, como usuários de mensagens e seções de perfil, podem não suportar a associação de nomes a identificadores de propriedade e podem retornar MAPI_E_NO_SUPPORT de **GetIDsFromNames**.
  
Se houver um erro que retorne um identificador para um nome específico, **GetIDsFromNames** retornará MAPI_W_ERRORS_RETURNED e define o tipo de propriedade na entrada da matriz de marca de propriedade que corresponde ao nome como **PT_ERROR** e ao identificador como zero. 
  
O mapeamento de nome para identificador é representado pela propriedade **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) de um objeto. **PR_MAPPING_SIGNATURE** contém uma [estrutura MAPIUID](mapiuid.md) que indica o provedor de serviços responsável pelo objeto. Se a **PR_MAPPING_SIGNATURE** propriedade for a mesma para dois objetos, suponha que esses objetos usem o mesmo mapeamento de nome para identificador. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Os identificadores que você passa de volta na matriz de marca de propriedade apontado pelo parâmetro  _lppPropNames_ devem estar no 0x8000 para 0xFFFE intervalo. As entradas nesta matriz devem estar na mesma ordem que os nomes passados na matriz de nomes de propriedade apontados por  _lppPropNames_. 
  
Se você suportar propriedades nomeadas em um contêiner, use o mesmo mapeamento de nome para identificador para todos os objetos em seu contêiner (ou seja, não use um mapeamento diferente para cada pasta em seu armazenamento de mensagens ou cada mensagem em sua pasta).
  
## <a name="notes-to-callers"></a>Notas para chamadores

Como os tipos de propriedade para os identificadores retornados na matriz de marca de propriedade apontados por  _lppPropTags_ são definidos como **PT_UNSPECIFIED**, você terá que chamar o método [IMAPIProp::SetProps](imapiprop-setprops.md) para recuperar os tipos precisos. 
  
Se você mover ou copiar objetos com propriedades nomeadas e os objetos de origem e destino têm assinaturas de mapeamento diferentes, conforme indicado pelos valores de suas propriedades **PR_MAPPING_SIGNATURE,** você deve preservar os nomes durante essas operações. Para preservar nomes de propriedade, ajuste os identificadores de propriedade correspondentes para corresponder ao mapeamento de nome para identificador do objeto de destino. 
  
Alguns objetos têm um limite quanto ao número de identificadores de propriedade que eles podem nomear. Se uma chamada para **GetIDsFromNames** faz com que esse limite seja excedido, o método retorna MAPI_E_TOO_BIG. Nesse caso, consulte por identificador. 
  
Para obter mais informações, consulte [MAPI Named Properties](mapi-named-properties.md). 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|SingleMAPIPropListCtrl.cpp  <br/> |CSingleMAPIPropListCtrl::FindAllNamedPropsUsed  <br/> |MFCMAPI usa o método **IMAPIProp::GetIDsFromNames** para obter marcas de propriedade para todas as propriedades nomeadas que foram mapeadas.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)
  
[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[MAPINAMEID](mapinameid.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[MAPI denominada propriedades](mapi-named-properties.md)
  
[Usando macros para tratamento de erros](using-macros-for-error-handling.md)

