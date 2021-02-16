---
title: Construindo identificadores de entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8d48c2584fa5b7e862102e401ea8165821607f77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427945"
---
# <a name="constructing-entry-identifiers"></a>Construindo identificadores de entrada

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os identificadores de entrada são construídos com a [estrutura ENTRYID.](entryid.md) A **estrutura ENTRYID** é composta por um sinalizador que descreve os atributos do identificador de entrada e o identificador de entrada real. 
  
## <a name="entryid-structure"></a>Estrutura ENTRYID

A **estrutura ENTRYID** é definida da seguinte forma: 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

MAPI_DIM é uma constante definida no arquivo de header MapiDefs.h. 
  
O primeiro byte do membro **abFlags** de 4 byte descreve o tipo e o uso do identificador de entrada e pode ter os seguintes valores: 
  
- MAPI_NOTRECI — Indica que o identificador de entrada não pode ser usado como um destinatário em uma mensagem.
    
- MAPI_NOTRESERVED — Indica que outros usuários não podem acessar o identificador de entrada.
    
- MAPI_NOW — Indica que o identificador de entrada não pode ser usado em outras ocasiões.
    
- MAPI_SHORTTERM — Indica que o identificador de entrada é de curto prazo. Todos os outros valores nesse byte devem ser definidos, a menos que outros usos do identificador de entrada sejam permitidos.
    
- MAPI_THISSESSION — Indica que o identificador de entrada não pode ser usado em outras sessões.
    
- MAPI_NOTRESERVED — Indica que o identificador de entrada pode ser usado por outros provedores de serviços para outros objetos.
    
O **ab** member of entry identifiers that is created by address book and message store providers is composed of two pieces: a 16-byte [MAPIUID](mapiuid.md) structure that identifies the service provider, and a piece to identify the object. **MAPIUID** é uma estrutura que contém um identificador global exclusivo, ou GUID. Um GUID é um identificador independente de ordem de byte que pode ser criado usando a ferramenta Criar *GUID** do Microsoft Visual Studio. 
  
Um provedor de serviços registra sua estrutura **MAPIUID** com MAPI durante o processo de logon em uma chamada para o método [IMAPISupport::SetProviderUID.](imapisupport-setprovideruid.md) Quando um cliente chama um **método OpenEntry** para acessar um objeto, o MAPI usa a estrutura **MAPIUID** para determinar qual provedor de serviços pode fornecer esse acesso. Os provedores de serviços devem usar a mesma **estrutura MAPIUID** para todas as versões de sua DLL. Isso permite que os clientes com a versão mais recente respondam a mensagens enviadas e salvas com a versão mais antiga. 
  
O restante do membro **ab** após o **MAPIUID** de 16 byte contém dados binários específicos do provedor de serviços para identificar objetos específicos. Não há nenhum tamanho fixo para essa parte do identificador de entrada. Pode ser de qualquer tamanho, dentro do motivo. Um provedor de serviços normalmente inclui as seguintes informações nesta parte de seus identificadores de entrada: 
  
- Informações de versão — Como é comum para um provedor de serviços alterar o formato de seus identificadores de entrada de versão para versão, o armazenamento de informações de versão possibilita determinar rapidamente como descobrir qualquer identificador de entrada.
    
- Informações de local — As informações de local são dados que dão a um provedor de serviços um indicador de como localizar o objeto representado pelo identificador de entrada. Por exemplo, um provedor de serviços pode armazenar o deslocamento de disco para o último local em um arquivo de dados em que o objeto foi armazenado. Como esse tipo de informação pode mudar ao longo do tempo, os provedores de serviços devem fornecer várias maneiras de localizar objetos em seus identificadores de entrada.
    
Embora os provedores de serviços possam reciclar seus identificadores de entrada, eles devem evitar essa prática. Se for necessário reutilizar um identificador de entrada, os provedores de serviços deverão tornar o período de tempo que se desdoba entre o uso inicial e a reutilização o máximo possível. Além disso, o identificador de entrada deve ser reatribuido a outro objeto do mesmo tipo. Ou seja, um identificador de entrada específico não deve ser associado primeiro a uma mensagem e, em seguida, a uma pasta.
  
## <a name="see-also"></a>Confira também



[Identificadores de entrada MAPI](mapi-entry-identifiers.md)

