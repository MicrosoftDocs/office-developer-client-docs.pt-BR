---
title: Criar identificadores de entradas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f15749077596bd6c89828eb730cadd5624a75fe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564581"
---
# <a name="constructing-entry-identifiers"></a>Criar identificadores de entradas

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Identificadores de entrada são construídos com a estrutura [ENTRYID](entryid.md) . A estrutura **ENTRYID** é composta por um sinalizador que descreve os atributos do identificador de entrada e o identificador de entrada real. 
  
## <a name="entryid-structure"></a>Estrutura ENTRYID

A estrutura **ENTRYID** é definida da seguinte maneira: 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

MAPI_DIM é uma constante que é definida no arquivo de cabeçalho MapiDefs.h. 
  
O primeiro byte do membro de 4 bytes **abFlags** descreve o tipo e use do identificador de entrada e pode ter os seguintes valores: 
  
- MAPI_NOTRECI — Indica o identificador de entrada não pode ser usada como um destinatário em uma mensagem.
    
- MAPI_NOTRESERVED — Indica de que outros usuários não podem acessar o identificador de entrada.
    
- MAPI_NOW — Indica de que o identificador de entrada não pode ser usado em outros momentos.
    
- MAPI_SHORTTERM — Indica de que o identificador de entrada é curto prazo. Todos os outros valores esse byte devem ser definidos, a menos que outros usos do identificador de entrada são permitidos.
    
- MAPI_THISSESSION — Indica de que o identificador de entrada não pode ser usado em outras sessões.
    
- MAPI_NOTRESERVED — Indica de que o identificador de entrada pode ser usado por outros provedores de serviços para outros objetos.
    
O membro de **ab** dos identificadores de entrada que é criado por provedores de repositório de mensagens e catálogo de endereços é composto por duas partes: uma estrutura [MAPIUID](mapiuid.md) de 16 bytes que identifica o provedor de serviço e uma informação para identificar o objeto. **MAPIUID** é uma estrutura que contém um identificador global exclusivo ou GUID. Um GUID é um identificador de independente da ordem de byte que pode ser criado usando o Microsoft Visual Studio*Criar GUID** ferramenta. 
  
Um provedor de serviços registra sua estrutura **MAPIUID** com MAPI durante o processo de logon em uma chamada ao método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) . Quando um cliente chama um método **OpenEntry** para acessar um objeto, o MAPI usa a estrutura **MAPIUID** para determinar quais serviços provedor pode fornecer a esse acesso. Provedores de serviços devem usar a mesma estrutura **MAPIUID** para todas as versões dos seu DLL. Isso permite que os clientes com a versão mais recente responder às mensagens enviadas e salvas com a versão mais antiga. 
  
O restante do membro **ab** após a 16 bytes **MAPIUID** contém específico do provedor de serviço de dados binários para identificar objetos específicos. Não há nenhum tamanho fixo para esta parte do identificador de entrada. Pode ser qualquer tamanho, dentro do motivo. Um provedor de serviços normalmente inclui as seguintes informações nesta parte do seus identificadores de entrada: 
  
- Informações sobre a versão — porque é comum para um provedor de serviço alterar o formato dos seus identificadores de entrada de versão para versão, armazenar informações de versão torna possível determinar rapidamente como decifrar qualquer identificador de entrada.
    
- Informações de local — informações de local são os dados que fornece um indicador de como localizar o objeto representado pelo identificador de entrada de um provedor de serviços. Por exemplo, um provedor de serviços pode armazenar o disco de deslocamento para o último lugar em um arquivo de dados que o objeto foi armazenado. Como esse tipo de informação pode mudar ao longo do tempo, provedores de serviços deverão fornecer várias maneiras para localizar os objetos em seus identificadores de entrada.
    
Embora os provedores de serviços podem reciclar seus identificadores de entrada, eles devem evitar essa prática. Se for necessário reutilizar um identificador de entrada, provedores de serviços devem fazer o período de tempo decorrido entre o uso inicial e a reutilização tanto quanto possível. Além disso, o identificador de entrada deve ser reatribuído a outro objeto do mesmo tipo. Ou seja, um identificador de entrada particular não deve ser associado primeiro uma mensagem e, em seguida, com uma pasta.
  
## <a name="see-also"></a>Confira também



[Identificadores de entrada MAPI](mapi-entry-identifiers.md)

