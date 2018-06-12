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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 1b55703c9ad12e3645e6e9cb3dcfcbdf21b90d25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766500"
---
# <a name="entryid"></a>ENTRYID

  
  
**Aplica-se a**: Outlook 
  
Contém um identificador de entrada para um objeto MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Macros relacionadas:  <br/> |[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md) <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a>Membros

 **abFlags**
  
> Bitmask dos sinalizadores que fornecem informações que descrevem o objeto. O primeiro byte dos sinalizadores, **abFlags [0]**, pode ser definido pelo provedor; as outras três são reservadas. Esses sinalizadores não devem ser definidos para os identificadores de entrada permanente; elas são definidas apenas para os identificadores de entrada de curto prazo. Para os clientes, esta estrutura é somente leitura. Sinalizadores a seguir podem ser definidos no **abFlags [0]**:
    
MAPI_NOTRECIP 
  
> O identificador de entrada não pode ser usado como um destinatário em uma mensagem.
    
MAPI_NOTRESERVED 
  
> Outros usuários não podem acessar o identificador de entrada.
    
MAPI_NOW 
  
> O identificador de entrada não pode ser usado em outros momentos.
    
MAPI_SHORTTERM 
  
> O identificador de entrada é curto prazo. Todos os outros valores esse byte devem ser definidos, a menos que outros usos do identificador de entrada estão habilitados.
    
MAPI_THISSESSION 
  
> O identificador de entrada não pode ser usado em outras sessões.
    
 **AB**
  
> Indica uma matriz de dados binários que são usados pelos provedores de serviço. O aplicativo cliente não pode usar essa matriz.
    
## <a name="remarks"></a>Coment�rios

A estrutura **ENTRYID** é usada por mensagem armazenar e provedores de catálogo para construir identificadores exclusivos para seus objetos de endereços. Identificadores de entrada são usados para identificar os seguintes tipos de objetos: 
  
- Repositórios de mensagem
    
- Pastas
    
- Mensagens
    
- Contêineres de catálogo de endereços
    
- Listas de distribuição
    
- Usuários de mensagens
    
- Objetos de status
    
- Seções de perfil
    
Cada provedor usa um formato para a estrutura de **ENTRYID** que faz sentido desse provedor. 
  
Os identificadores de entrada não podem ser comparados diretamente porque um objeto pode ser representado por dois valores binários diferentes. Para determinar se os dois identificadores de entrada representam o mesmo objeto, chame o método [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) . 
  
Quando um cliente chama um método do objeto [IMAPIProp::GetProps](imapiprop-getprops.md) para recuperar seu identificador de entrada, o objeto retorna o formulário mais permanente do identificador de entrada. Um cliente pode verificar se um identificador de entrada é longo prazo, verificando se nenhum dos sinalizadores estão definidas no primeiro byte do membro **abFlags** . 
  
Quando um cliente acessa um identificador de entrada por meio de uma coluna em uma tabela, provavelmente que esse identificador de entrada é curto prazo, em vez de longo prazo. Identificadores de entrada de curto prazo podem ser usados para abrir seus objetos correspondentes apenas na sessão MAPI atual. Um cliente pode verificar se um identificador de entrada é curto prazo, verificando se todos os sinalizadores estão definidos no primeiro byte do membro **abFlags** . 
  
Alguns identificadores de entrada são a curto prazo, mas tem o uso de longo prazo. Tal um identificador de entrada terá um ou mais dos sinalizadores apropriados definidos no primeiro byte do seu membro **abFlags** . 
  
Uma estrutura **ENTRYID** é semelhante a uma estrutura [FLATENTRY](flatentry.md) . No entanto, há algumas diferenças: 
  
- Uma estrutura **ENTRYID** não armazena o tamanho do identificador de entrada; uma estrutura **FLATENTRY** faz. 
    
- Uma estrutura **ENTRYID** armazena os dados de sinalizador e o restante do identificador de entrada separadamente; uma estrutura **FLATENTRY** armazena os dados de sinalizador com o restante do identificador de entrada. 
    
- Uma estrutura **ENTRYID** é passada como um parâmetro para os métodos da interface [IMAPIProp](imapipropiunknown.md) e para os seguintes métodos **OpenEntry** : [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry ](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- Uma estrutura **ENTRYID** é usada para armazenar um identificador de entrada no disco. Uma estrutura **FLATENTRY** é usada para armazenar um identificador de entrada em um arquivo ou passá-la em um fluxo de bytes. 
    
Clientes sempre devem passar em identificadores de entrada naturalmente alinhado. Embora provedores devem lidar com identificadores de entrada arbitrariamente alinhado, os clientes não devem esperar que esse comportamento. Falha ao passar um identificador de entrada alinhado bom para um método pode causar uma falha de alinhamento em processadores RISC. 
  
O fator de alinhamento natural, geralmente 8 bytes, é o tipo de dados maior suportado pela CPU e geralmente o mesmo fator de alinhamento usado pelo alocador de memória do sistema. Um endereço de memória naturalmente alinhado permite a CPU acessar qualquer tipo de dados suporta nesse endereço sem gerar uma falha de alinhamento. Para CPUs RISC, um tipo de dados de tamanho N bytes geralmente deve ser alinhado em um múltiplo de bytes N, com o endereço sendo um múltiplo par de N.
  
Para obter mais informações, consulte [Identificadores de entrada](mapi-entry-identifiers.md). 
  
## <a name="see-also"></a>Confira também



[FLATENTRY](flatentry.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[Propriedade canônico de PidTagRecordKey](pidtagrecordkey-canonical-property.md)


[Estruturas MAPI](mapi-structures.md)

