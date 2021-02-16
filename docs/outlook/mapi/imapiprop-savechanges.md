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
  
Faz alterações permanentes que foram feitas em um objeto desde a última operação de salvar. 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla o que acontece com o objeto quando o método **IMAPIProp::SaveChanges** é chamado. Os sinalizadores a seguir podem ser definidos: 
    
NON_EMS_XP_SAVE
  
> Indica que a mensagem não foi entregue de um Microsoft Exchange Server. Esse sinalizador deve ser usado em combinação com o método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) e o sinalizador ITEMPROC_FORCE para indicar a um armazenamento PST que a mensagem está qualificada para processamento de regras antes que o armazenamento do arquivo de Pastas Particulares (PST) notifique qualquer cliente ouvinte de que a mensagem chegou. Esse processamento de regras só se aplica a novas mensagens criadas com [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) em um servidor que não seja um Exchange Server. Nesse caso, o Exchange Server já teria processado regras na mensagem. 
    
FORCE_SAVE 
  
> As alterações devem ser escritas no objeto, substituindo quaisquer alterações anteriores feitas no objeto, e o objeto deve ser fechado. A permissão de leitura/gravação deve ser definida para que a operação seja bem-sucedida. O FORCE_SAVE sinalizador é usado após uma chamada anterior para **SaveChanges** retornada MAPI_E_OBJECT_CHANGED. 
    
KEEP_OPEN_READONLY 
  
> As alterações devem ser comprometidas e o objeto deve ser mantido aberto para leitura. Nenhuma alteração adicional será feita. 
    
KEEP_OPEN_READWRITE 
  
> As alterações devem ser comprometidas e o objeto deve ser mantido aberto para permissão de leitura/gravação. Esse sinalizador geralmente é definido quando o objeto foi aberto pela primeira vez para permissão de leitura/gravação. Alterações subsequentes no objeto são permitidas. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **SaveChanges** retorne com êxito, possivelmente antes que as alterações tenham sido totalmente comprometidas. 
    
SPAMFILTER_ONSAVE
  
> Habilita a filtragem de spam em uma mensagem que está sendo salva. O suporte à filtragem de spam está disponível somente se o tipo de endereço de email do remetente for SMTP(Simple Mail Transfer Protocol) e a mensagem estiver sendo salva em um repositório de um arquivo de pastas particulares (PST).
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O compromisso das alterações foi bem-sucedido.
    
MAPI_E_NO_ACCESS 
  
> **SaveChanges** não poderá manter o objeto aberto para permissão somente leitura se KEEP_OPEN_READONLY estiver definida ou permissão de leitura/gravação se KEEP_OPEN_READWRITE estiver definida. Nenhuma alteração foi comprometida. 
    
MAPI_E_OBJECT_CHANGED 
  
> O objeto foi alterado desde que foi aberto.
    
MAPI_E_OBJECT_DELETED 
  
> O objeto foi excluído desde que foi aberto.
    
## <a name="remarks"></a>Comentários

O **método IMAPIProp::SaveChanges** torna as alterações de propriedade permanentes para objetos que suportam o modelo de transação de processamento, como mensagens, anexos, contêineres de livro de endereços e objetos de usuário de mensagens. Os objetos que não suportam transações, como pastas, armazenamentos de mensagens e seções de perfil, fazem alterações permanentemente imediatamente. Nenhuma chamada **para SaveChanges** é necessária. 
  
Como os provedores de serviços não precisarão gerar um identificador de entrada para seus objetos até que todas as propriedades tenham sido salvas, a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de um objeto pode não estar disponível até que o método **SaveChanges** tenha sido chamado. Alguns provedores aguardam até que KEEP_OPEN_READONLY sinalizador seja definido na **chamada SaveChanges.** KEEP_OPEN_READONLY indica que as alterações a serem salvas na chamada atual serão as últimas alterações que serão feitas no objeto. 
  
Algumas implementações de armazenamento de mensagens não mostram mensagens recém-criadas em uma pasta até que um cliente salve as alterações de mensagem usando **SaveChanges** e libere os objetos de mensagem usando o método [IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) Além disso, algumas implementações de objeto não podem gerar uma propriedade PR_ENTRYID para um objeto recém-criado até que **SaveChanges** tenha sido chamado, e algumas podem fazer isso somente depois que **SaveChanges** tiver sido chamado usando um conjunto de **KEEP_OPEN_READONLY** em _ulFlags_.
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se você receber o KEEP_OPEN_READONLY sinalizador, terá a opção de deixar o acesso do objeto como leitura/gravação. No entanto, um provedor nunca pode deixar um objeto em um estado somente leitura quando o sinalizador KEEP_OPEN_READWRITE é passado.
  
Quando um cliente salva vários anexos em várias mensagens, ele chama o **método SaveChanges** para cada anexo e cada mensagem. Muitas vezes, os clientes MAPI_DEFERRED_ERRORS para cada uma dessas chamadas, exceto para a última. Você pode retornar erros com a última chamada ou chamadas anteriores. Você pode até ignorar o sinalizador. 
  
Se o KEEP_OPEN_READWRITE ou KEEP_OPEN_READONLY for definido junto com o MAPI_DEFERRED_ERRORS, você poderá ignorar a solicitação de adiamento de erro. Se MAPI_DEFERRED_ERRORS não estiver definido em _ulFlags_, um dos erros adiados anteriormente poderá ser retornado para a **chamada SaveChanges.** 
  
Se um provedor de transporte remoto fornece uma implementação funcional desse método é opcional e depende de outras opções de design em sua implementação. Se você implementar esse método, faça isso de acordo com a documentação aqui. Como os objetos de pasta e os objetos de status não são transacionados, no mínimo a implementação do **SaveChanges** de um provedor de transporte remoto deve retornar S_OK sem realmente fazer qualquer trabalho. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se um cliente passar KEEP_OPEN_READONLY, chamar o método [IMAPIProp::SetProps](imapiprop-setprops.md) e chamar **SaveChanges** novamente, a mesma implementação poderá falhar. 
  
Depois de MAPI_E_NO_ACCESS de uma chamada na qual você definiu KEEP_OPEN_READWRITE, você continuará a ter permissão de leitura/gravação para o objeto. Você pode chamar **SaveChanges** novamente, passando o sinalizador KEEP_OPEN_READONLY ou nenhum sinalizador com KEEP_OPEN_SUFFIX. 
  
Se um provedor oferece suporte KEEP_OPEN_READWRITE sinalizador depende da implementação do provedor. 
  
Para indicar que a única chamada a ser feita no objeto após **SaveChanges** é **IUnknown::Release**, não defina sinalizadores para o _parâmetro ulFlags._ Um erro de **SaveChanges** indica que não foi possível tornar permanentes as alterações pendentes. Provedores diferentes lidam com a ausência de sinalizadores na chamada **SaveChanges** de maneira diferente. Alguns provedores tratam esse estado da mesma forma que KEEP_OPEN_READONLY; outros provedores o interpretam da mesma forma que KEEP_OPEN_READWRITE. Ainda outros provedores desligaram o objeto quando não recebem sinalizadores na **chamada SaveChanges.** 
  
Algumas propriedades, normalmente computadas, não podem ser processadas até que você chame **SaveChanges** e, em alguns casos, **Release**.
  
Ao fazer alterações em massa, como salvar anexos em várias mensagens, adia o processamento de erros definindo o sinalizador MAPI_DEFERRED_ERRORS em  _ulFlags_. Se você salvar vários anexos em várias mensagens, faça uma chamada **SaveChanges** para cada anexo e uma **chamada SaveChanges** para cada mensagem. De definida a MAPI_DEFERRED_ERRORS sinalizador para cada chamada de anexo e para todas as mensagens, exceto a última. 
  
Se **SaveChanges** retornar MAPI_E_OBJECT_CHANGED, verifique se o objeto original foi modificado. Nesse caso, avise o usuário, que pode solicitar que as alterações sobrescrevem as alterações anteriores ou salve o objeto em outro lugar. Se o objeto original tiver sido excluído, avise o usuário para dar a ele a oportunidade de salvar o objeto em outro local. 
  
Você não pode **chamar SaveChanges** com o FORCE_SAVE sinalizador em um objeto aberto que foi excluído. 
  
Se **SaveChanges** retornar um erro, o objeto cujas alterações devem ser salvas permanece aberto, independentemente dos sinalizadores definidos no _parâmetro ulFlags._ 
  
> [!IMPORTANT]
> O  _ulFlags_ NON_EMS_XP_SAVE e SPAMFILTER_ONSAVE podem não ser definidos no arquivo de header baixável que você tem atualmente, nesse caso, você pode adicioná-lo ao seu código usando os seguintes valores: >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`
  
Para obter mais informações, consulte [Salvar propriedades MAPI](saving-mapi-properties.md).
  
## <a name="see-also"></a>Confira também



[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[Propriedade canônica PidTagEntryId](pidtagentryid-canonical-property.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Salvando propriedades MAPI](saving-mapi-properties.md)

