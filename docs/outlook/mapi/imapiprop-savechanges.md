---
title: IMAPIPropSaveChanges
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SaveChanges
api_type:
- COM
ms.assetid: 864dbc3e-2039-435a-a279-385d79d1d13f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2c8244180a5cafedc887fa72f36f233fb5084f79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316629"
---
# <a name="imapipropsavechanges"></a>IMAPIProp::SaveChanges

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Torna permanente quaisquer alterações feitas a um objeto desde a última operação de salvamento. 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Uma bitmask de sinalizadores que controlam o que acontece com o objeto quando o método **IMAPIProp:: SaveChanges** é chamado. Os seguintes sinalizadores podem ser definidos: 
    
NON_EMS_XP_SAVE
  
> Indica que a mensagem não foi entregue de um servidor do Microsoft Exchange. Esse sinalizador deve ser usado em combinação com o método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) e o sinalizador ITEMPROC_FORCE para indicar a um repositório PST que a mensagem está qualificada para o processamento de regras antes que o repositório de arquivos de pastas particulares (PST) Notifique qualquer cliente de escuta que a mensagem chegou. Este processamento de regras só se aplica a novas mensagens criadas com o [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) em um servidor que não é um servidor Exchange, caso em que o servidor Exchange já tenha processado as regras da mensagem. 
    
FORCE_SAVE 
  
> As alterações devem ser gravadas no objeto, substituindo todas as alterações anteriores que foram feitas no objeto e o objeto deve ser fechado. A permissão de leitura/gravação deve ser definida para que a operação seja bem-sucedida. O sinalizador FORCE_SAVE é usado depois que uma chamada anterior a **SaveChanges** retornou MAPI_E_OBJECT_CHANGED. 
    
KEEP_OPEN_READONLY 
  
> As alterações devem ser confirmadas e o objeto deve ser mantido aberto para leitura. Nenhuma alteração adicional será feita. 
    
KEEP_OPEN_READWRITE 
  
> As alterações devem ser confirmadas e o objeto deve ser mantido aberto para permissão de leitura/gravação. Normalmente, esse sinalizador é definido quando o objeto foi aberto pela primeira vez para permissões de leitura/gravação. Alterações subsequentes no objeto são permitidas. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **SaveChanges** seja retornado com êxito, possivelmente antes de as alterações terem sido totalmente confirmadas. 
    
SPAMFILTER_ONSAVE
  
> Habilita a filtragem de spam em uma mensagem que está sendo salva. O suporte à filtragem de spam está disponível somente se o tipo de endereço de email do remetente for SMTP(Simple Mail Transfer Protocol) e a mensagem estiver sendo salva em um repositório de um arquivo de pastas particulares (PST).
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O compromisso das alterações foi bem-sucedido.
    
MAPI_E_NO_ACCESS 
  
> **SaveChanges** não pode manter o objeto aberto para permissão somente leitura se KEEP_OPEN_READONLY estiver definido, ou permissão de leitura/gravação se KEEP_OPEN_READWRITE estiver definido. Nenhuma alteração é confirmada. 
    
MAPI_E_OBJECT_CHANGED 
  
> O objeto foi alterado desde que foi aberto.
    
MAPI_E_OBJECT_DELETED 
  
> O objeto foi excluído desde que foi aberto.
    
## <a name="remarks"></a>Comentários

O método **IMAPIProp:: SaveChanges** torna as alterações de propriedade permanentes para objetos que dão suporte ao modelo de transação de processamento, como mensagens, anexos, contêineres de catálogo de endereços e objetos de usuário de mensagens. Objetos que não dão suporte a transações, como pastas, repositórios de mensagens e seções de perfil, tornam as alterações permanentes imediatamente. Nenhuma chamada para **SaveChanges** é necessária. 
  
Como os provedores de serviços não precisam gerar um identificador de entrada para seus objetos até que todas as propriedades tenham sido salvas, a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de um objeto pode não estar disponível até que o método **SaveChanges** foi chamado. Alguns provedores esperam até que o sinalizador KEEP_OPEN_READONLY seja definido na chamada **SaveChanges** . KEEP_OPEN_READONLY indica que as alterações a serem salvas na chamada atual serão as últimas alterações que serão feitas no objeto. 
  
Algumas implementações de repositório de mensagens não mostram mensagens recém-criadas em uma pasta até que um cliente salve as alterações de mensagens usando **SaveChanges** e libere os objetos de mensagem usando o método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) . Além disso, algumas implementações de objeto não podem gerar uma propriedade **PR_ENTRYID** para um objeto recém-criado até que **SaveChanges** tenha sido chamado, e alguns podem fazer isso somente depois que **SaveChanges** tiver sido chamado usando o KEEP_OPEN_READONLY definido no _parâmetroulflags_.
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se você receber o sinalizador KEEP_OPEN_READONLY, terá a opção de deixar o acesso do objeto como leitura/gravação. No enTanto, um provedor nunca pode deixar um objeto em um estado somente leitura quando o sinalizador KEEP_OPEN_READWRITE é passado.
  
Quando um cliente salva vários anexos em várias mensagens, ele chama o método **SaveChanges** para todos os anexos e todas as mensagens. Geralmente, os clientes definirão MAPI_DEFERRED_ERRORS para cada uma dessas chamadas, exceto para o último. Você pode retornar erros com a última chamada ou chamadas anteriores. Você pode até mesmo ignorar o sinalizador. 
  
Se KEEP_OPEN_READWRITE ou KEEP_OPEN_READONLY estiver definido junto com o MAPI_DEFERRED_ERRORS, você poderá ignorar a solicitação de diferimento de erro. Se MAPI_DEFERRED_ERRORS não estiver definido no _parâmetroulflags_, um dos erros adiados anteriormente poderá ser retornado para a chamada **SaveChanges** . 
  
Se um provedor de transporte remoto fornece uma implementação funcional desse método é opcional e depende de outras escolhas de design na sua implementação. Se você implementar esse método, faça-o de acordo com a documentação aqui. Como objetos Folder e status objetos não são transacionados, no mínimo uma implementação de **SaveChanges** do provedor de transporte remoto deve retornar S_OK sem realmente realizar qualquer trabalho. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se um cliente passar KEEP_OPEN_READONLY, chama o método [IMAPIProp::](imapiprop-setprops.md) SetProps e, em seguida, chama **SaveChanges** novamente, a mesma implementação pode falhar. 
  
Após receber MAPI_E_NO_ACCESS de uma chamada na qual você definiu KEEP_OPEN_READWRITE, você continuará com permissão de leitura/gravação para o objeto. Você pode chamar o **SaveChanges** novamente, passando o sinalizador KEEP_OPEN_READONLY ou nenhum sinalizador com KEEP_OPEN_SUFFIX. 
  
Se um provedor oferece suporte ao sinalizador KEEP_OPEN_READWRITE depende da implementação do provedor. 
  
Para indicar que a única chamada a ser feita no objeto após **SaveChanges** é **IUnknown:: Release**, configure nenhum sinalizador para o parâmetro _parâmetroulflags_ . Um erro de **SaveChanges** indica que não foi possível tornar as alterações pendentes permanentes. Diferentes provedores manipulam a ausência de sinalizadores na chamada **SaveChanges** de forma diferente. Alguns provedores tratam esse estado da mesma forma que KEEP_OPEN_READONLY; outros provedores interpretam o mesmo que KEEP_OPEN_READWRITE. Ainda outros provedores desligam o objeto quando não recebem sinalizadores na chamada **SaveChanges** . 
  
Algumas propriedades, normalmente, Propriedades computadas, não podem ser processadas até que você chame **SaveChanges** e, em alguns casos, o **lançamento**.
  
Ao fazer alterações em massa, como salvar anexos em várias mensagens, adie o processamento de erro definindo o sinalizador MAPI_DEFERRED_ERRORS no _parâmetroulflags_. Se você salvar vários anexos em várias mensagens, faça uma chamada **SaveChanges** para cada anexo e uma chamada **SaveChanges** para cada mensagem. Defina o sinalizador MAPI_DEFERRED_ERRORS para cada chamada de anexo e para todas as mensagens, exceto a última. 
  
Se **SaveChanges** retornar MAPI_E_OBJECT_CHANGED, verifique se o objeto original foi modificado. Em caso afirmativo, avise ao usuário que pode solicitar que as alterações substituam as alterações anteriores ou salvem o objeto em outro lugar. Se o objeto original tiver sido excluído, avise o usuário para dar a eles a oportunidade de salvar o objeto em outro local. 
  
Você não pode chamar **SaveChanges** com o sinalizador FORCE_SAVE em um objeto Open que tenha sido excluído. 
  
Se **SaveChanges** retornar um erro, o objeto cujas alterações foram salvas permanecerá aberto, independentemente dos sinalizadores definidos no parâmetro _parâmetroulflags_ . 
  
> [!IMPORTANT]
> O _parâmetroulflags_ NON_EMS_XP_SAVE e o SPAMFILTER_ONSAVE podem não ser definidos no arquivo de cabeçalho baixável que você tem atualmente e, nesse caso, você pode adicioná-lo ao seu código usando os seguintes valores: >`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`
  
Para obter mais informações, consulte [salvar propriedades MAPI](saving-mapi-properties.md).
  
## <a name="see-also"></a>Confira também



[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[Propriedade canônica PidTagEntryId](pidtagentryid-canonical-property.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Salvar propriedades MAPI](saving-mapi-properties.md)

