---
title: ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ENTRYID
api_type:
- COM
ms.assetid: 8ebb21ca-5ad1-4dcc-97b6-2390664b5d8d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c77acb5226361ce31a7f6b1694de7fe23f8dd71b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415268"
---
# <a name="entryid"></a>ENTRYID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um identificador de entrada para um objeto MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Macros relacionadas:  <br/> |[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md) <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a>Members

 **abFlags**
  
> Bitmask de sinalizadores que fornecem informações que descrevem o objeto. Somente o primeiro byte dos sinalizadores, **abFlags [0]**, pode ser definido pelo provedor; os outros três são reservados. Esses sinalizadores não devem ser definidos para identificadores de entradas permanentes; Eles são definidos apenas para identificadores de entrada de curto prazo. Para clientes, essa estrutura é somente leitura. Os seguintes sinalizadores podem ser definidos no **abFlags [0]**:
    
MAPI_NOTRECIP 
  
> O identificador de entrada não pode ser usado como um destinatário em uma mensagem.
    
MAPI_NOTRESERVED 
  
> Outros usuários não podem acessar o identificador de entrada.
    
MAPI_NOW 
  
> O identificador de entrada não pode ser usado em outros momentos.
    
MAPI_SHORTTERM 
  
> O identificador de entrada é de curto prazo. Todos os outros valores nesse byte devem ser definidos, a menos que outros usos do identificador de entrada estejam habilitados.
    
MAPI_THISSESSION 
  
> O identificador de entrada não pode ser usado em outras sessões.
    
 **AB**
  
> Indica uma matriz de dados binários que é usada por provedores de serviços. O aplicativo cliente não pode usar essa matriz.
    
## <a name="remarks"></a>Comentários

A **** estrutura ENTRYID é usada por provedores de repositório de mensagens e de catálogo de endereços para construir identificadores exclusivos para seus objetos. Os identificadores de entrada são usados para identificar os seguintes tipos de objetos: 
  
- Repositórios de mensagens
    
- Folders
    
- Mensagens
    
- Contêineres do catálogo de endereços
    
- Listas de distribuição
    
- Usuários de mensagens
    
- Objetos de status
    
- Seções de perfil
    
Cada provedor usa um formato para a **** estrutura ENTRYID que faz sentido para esse provedor. 
  
Os identificadores de entrada não podem ser comparados diretamente porque um objeto pode ser representado por dois valores binários diferentes. Para determinar se dois identificadores de entrada representam o mesmo objeto, chame o método [IMAPISession:: CompareEntryIDs](imapisession-compareentryids.md) . 
  
Quando um cliente chama o método [IMAPIProp::](imapiprop-getprops.md) GetProps de um objeto para recuperar seu identificador de entrada, o objeto retorna a forma mais permanente do identificador de entrada. Um cliente pode verificar se um identificador de entrada é de longo prazo, verificando se nenhum dos sinalizadores está definido no primeiro byte do membro **abFlags** . 
  
Quando um cliente acessa um identificador de entrada por meio de uma coluna em uma tabela, provavelmente esse identificador de entrada é de curto prazo em vez de longo prazo. Identificadores de entrada de curto prazo podem ser usados para abrir seus objetos correspondentes apenas na sessão MAPI atual. Um cliente pode verificar se um identificador de entrada é de curto prazo verificando se todos os sinalizadores estão definidos no primeiro byte do membro **abFlags** . 
  
Alguns identificadores de entrada são de curto prazo, mas têm uso de longo prazo. Esse identificador de entrada terá um ou mais dos sinalizadores apropriados definidos no primeiro byte de seu membro **abFlags** . 
  
Uma **** estrutura ENTRYID é semelhante a uma estrutura [FLATENTRY](flatentry.md) . No enTanto, há algumas diferenças: 
  
- Uma **** estrutura ENTRYID não armazena o tamanho do identificador de entrada; uma estrutura **FLATENTRY** . 
    
- Uma **** estrutura ENTRYID armazena os dados de sinalizador e o restante do identificador de entrada separadamente; uma estrutura **FLATENTRY** armazena os dados de sinalizador com o resto do identificador de entrada. 
    
- Uma **** estrutura ENTRYID é passada como um parâmetro para os métodos da interface [IMAPIProp](imapipropiunknown.md) e para os seguintes métodos **OpenEntry** : [IABLogon:: OpenEntry](iablogon-openentry.md), [IAddrBook:: OpenEntry](iaddrbook-openentry.md), [IMAPIContainer:: OpenEntry ](imapicontainer-openentry.md), [IMAPISession:: OpenEntry](imapisession-openentry.md), [IMAPISupport:: OpenEntry](imapisupport-openentry.md), [IMsgStore:: OpenEntry](imsgstore-openentry.md), [IMSLogon::](imslogon-openentry.md) OpenEntry
    
- Uma **** estrutura ENTRYID é usada para armazenar um identificador de entrada no disco. Uma estrutura **FLATENTRY** é usada para armazenar um identificador de entrada em um arquivo ou passá-lo em um fluxo de bytes. 
    
Os clientes devem sempre passar por identificadores de entrada alinhados naturalmente. Embora os provedores manipulem identificadores de entrada com alinhamento arbitrária, os clientes não devem esperar esse comportamento. A falha ao passar um identificador de entrada alinhada para um método pode causar uma falha de alinhamento nos processadores RISC. 
  
O fator de alinhamento natural, geralmente 8 bytes, é o maior tipo de dados suportado pela CPU e, normalmente, o mesmo fator de alinhamento usado pelo alocador de memória do sistema. Um endereço de memória logicamente alinhado permite que a CPU acesse qualquer tipo de dados compatível com esse endereço sem gerar uma falha de alinhamento. Para CPUs RISC, um tipo de dados de tamanho N bytes geralmente deve ser alinhado em um múltiplo par de N bytes, sendo que o endereço é um múltiplo de N.
  
Para obter mais informações, consulte identificadores de [entrada](mapi-entry-identifiers.md). 
  
## <a name="see-also"></a>Confira também



[FLATENTRY](flatentry.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[Propriedade canônica PidTagRecordKey](pidtagrecordkey-canonical-property.md)


[Estruturas MAPI](mapi-structures.md)

