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
  
Os identificadores de entrada são construídos [](entryid.md) com a estrutura ENTRYID. A **** estrutura ENTRYID é composta de um sinalizador que descreve os atributos do identificador de entrada e o identificador de entrada real. 
  
## <a name="entryid-structure"></a>Estrutura ENTRYid

A **** estrutura ENTRYID é definida da seguinte maneira: 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

MAPI_DIM é uma constante definida no arquivo de cabeçalho MapiDefs. h. 
  
O primeiro byte do membro **abFlags** de 4 bytes descreve o tipo e o uso do identificador de entrada e pode ter os seguintes valores: 
  
- MAPI_NOTRECI — indica que o identificador de entrada não pode ser usado como um destinatário em uma mensagem.
    
- MAPI_NOTRESERVED — indica que outros usuários não podem acessar o identificador de entrada.
    
- MAPI_NOW — indica que o identificador de entrada não pode ser usado em outros momentos.
    
- MAPI_SHORTTERM — indica que o identificador de entrada é de curto prazo. Todos os outros valores nesse byte devem ser definidos, a menos que outros usos do identificador de entrada sejam permitidos.
    
- MAPI_THISSESSION — indica que o identificador de entrada não pode ser usado em outras sessões.
    
- MAPI_NOTRESERVED — indica que o identificador de entrada pode ser usado por outros provedores de serviços para outros objetos.
    
O membro **AB** dos identificadores de entrada criados por catálogo de endereços e provedores de repositório de mensagens é composto por duas partes: uma estrutura [MAPIUID](mapiuid.md) de 16 bytes que identifica o provedor de serviços e uma peça para identificar o objeto. **MAPIUID** é uma estrutura que contém um identificador global exclusivo ou GUID. Um GUID é um identificador independente de ordem de bytes que pode ser criado usando o Microsoft Visual Studio*Create GUID** Tool. 
  
Um provedor de serviços registra sua estrutura do **MAPIUID** com MAPI durante o processo de logon em uma chamada para o método [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) . Quando um cliente chama um método **OpenEntry** para acessar um objeto, MAPI usa a estrutura **MAPIUID** para determinar qual provedor de serviços pode fornecer esse acesso. Os provedores de serviços devem usar a mesma estrutura **MAPIUID** para todas as versões de sua dll. Isso permite que os clientes com a versão mais recente respondam às mensagens enviadas e salvas com a versão mais antiga. 
  
O restante do membro **AB** após a **MAPIUID** de 16 bytes contém dados binários específicos do provedor de serviços para identificar objetos específicos. Não há tamanho fixo para esta parte do identificador de entrada. Pode ser qualquer tamanho, dentro da razão. Um provedor de serviços normalmente inclui as seguintes informações nesta parte de seus identificadores de entrada: 
  
- Informações de versão — como é comum que um provedor de serviços altere o formato de seus identificadores de entrada da versão para a versão, armazenar informações de versão permite determinar rapidamente como decifrar qualquer identificador de entrada.
    
- Informações de local-informações de local são dados que fornecem um provedor de serviços um indicador de como localizar o objeto representado pelo identificador de entrada. Por exemplo, um provedor de serviços pode armazenar o deslocamento do disco para o último local em um arquivo de dados que o objeto foi armazenado. Como esse tipo de informação pode mudar com o tempo, os provedores de serviços devem fornecer várias maneiras de localizar objetos em seus identificadores de entrada.
    
Embora os provedores de serviços possam reciclar seus identificadores de entrada, eles devem evitar essa prática. Se for necessário reutilizar um identificador de entrada, os provedores de serviços devem tornar o período de tempo decorrido entre o uso inicial e a reutilização o máximo possível. Além disso, o identificador de entrada deve ser reatribuído a outro objeto do mesmo tipo. Ou seja, um determinado identificador de entrada não deve ser associado primeiro a uma mensagem e, em seguida, com uma pasta.
  
## <a name="see-also"></a>Confira também



[Identificadores de entrada MAPI](mapi-entry-identifiers.md)

