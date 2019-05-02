---
title: XML para amigos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3362639a-8098-47ab-ba94-ee89e4920032
description: O elemento friends no esquema XML do provedor Microsoft Outlook Social Connector (OSC) permite que um provedor OSC especifique informações para uma lista de pessoas associadas a um usuário do Outlook na rede social.
ms.openlocfilehash: df3bf03c5fd1dcdac3096411bc60bcb1eeec661e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361156"
---
# <a name="xml-for-friends"></a>XML para amigos

O elemento **friends** no esquema XML do provedor Microsoft Outlook Social Connector (OSC) permite que um provedor OSC especifique informações para uma lista de pessoas associadas a um usuário do Outlook na rede social. Se o provedor OSC der suporte à sincronização em cache, essa lista de pessoas conterá apenas os amigos do usuário do Outlook na rede social. Se o OSC der suporte à sincronização por demanda ou híbrida, essa lista poderá conter amigos e não amigos do usuário do Outlook. 

Cada pessoa na lista é representada como um elemento **person** no esquema XML, que dá suporte a detalhes como nome, sobrenome e endereços de e-mail. Os provedores OSC usam os elementos **friends** e **person** independentemente de como eles querem que o OSC sincronize as informações de amigos da rede social. Observe que os elementos filho de **person** são semelhantes a algumas das propriedades de um contato do Outlook, o que facilita o armazenamento de amigos em uma pasta de contatos do Outlook, específica para a rede social, se a rede social der suporte à sincronização híbrida ou em cache de amigos para uma pasta de contatos do Outlook. 

## <a name="example-scenarios"></a>Exemplos de cenários

Os cenários de exemplo a seguir mostram as chamadas à API de extensibilidade do provedor OSC que um provedor OSC implementa e o OSC faz para obter informações de amigos. As informações são expressas em cadeias de caracteres XML que estão em conformidade com o esquema XML do provedor OSC.
  
Confira um exemplo de XML de amigos em [Exemplo XML de amigos](friends-xml-example.md). Saiba mais sobre como sincronizar informações de amigos em [sincronização de amigos e atividades](synchronizing-friends-and-activities.md).

### <a name="scenario-1-get-a-list-of-friends"></a>Cenário 1: obter uma lista de amigos

Cenário 1: o OSC obtém uma lista de amigos, um objeto [ISocialPerson](isocialpersoniunknown.md) e uma imagem de cada amigo: 
    
1. Um provedor OSC que dá suporte à exibição de amigos do site da rede social e permite que o OSC armazene em cache as informações de amigos indica isso ao OSC usando os elementos **getFriends** e **cacheFriends**, que são elementos filho do elemento **capabilities**. 
    
2. O provedor OSC também implementa os métodos [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), [ISocialSession::GetPerson](isocialsession-getperson.md), [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) e [ISocialPerson::GetPicture](isocialperson-getpicture.md). 
    
3. O OSC chama o **ISocialProvider::GetCapabilities** para verificar o valor dos seguintes elementos: **getFriends**, para verificar se o provedor OSC der suporte à exibição de amigos da rede social, e **cacheFriends** para verificar se o provedor der suporte a amigos com armazenamento em cache. 
    
4. O OSC chama o **ISocialSession::GetPerson** para obter um objeto **ISocialPerson** para o usuário do Outlook. 
    
5. O OSC chama o **ISocialPerson::GetFriendsAndColleagues** para obter a lista de amigos do usuário do Outlook retornada na cadeia de caracteres do parâmetro _personCollection_. A cadeia de caracteres _personCollection_ está em conformidade com a definição do esquema XML para o elemento **friends** no esquema XML. 
    
6. Para cada amigo na cadeia de caracteres XML _personCollection_, o OSC obtém o valor do elemento **userID** para chamar **ISocialSession::GetPerson** para obter um objeto **ISocialPerson** para esse amigo. 
    
7. Para cada amigo na cadeia de caracteres XML **personCollection**, o OSC chama [ISocialPerson::GetPicture](isocialperson-getpicture.md) para obter um recurso de imagem para esse amigo. 
    
   O OSC pode fazer chamadas adicionais no objeto **ISocialPerson** para obter atividades e detalhes (por exemplo, endereços de e-mail) desse amigo. 
    
### <a name="scenario-2-synchronize-friends"></a>Cenário 2: sincronizar amigos 

Cenário 2 — o OSC sincroniza amigos dinamicamente:
    
1. O provedor OSC que dá suporte à sincronização sob demanda de amigos e não amigos indica isso para o OSC usando os elementos **getFriends** e **dynamicContactsLookup**. O provedor OSC também define o elemento **hashFunction**. Todos os três elementos são elementos filhos de **capabilities**. 
    
2. O provedor OSC também implementa o método [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md). 
    
3. O OSC chama **ISocialProvider::GetCapabilities** para verificar os valores de **getFriends** e **dynamicContactsLookup** a fim de examinar se o provedor OSC der suporte a amigos e à sincronização sob demanda de amigos e não amigos. O OSC também cria uma nota do valor de **hashFunction** com suporte no provedor OSC. 
    
4. Para cada usuário exibido no Painel de Pessoas, o OSC coleta o endereço de e-mail do usuário e o criptografa usando a função hash especificada em **hashFunction**. Isso forma uma cadeia de caracteres XML que está em conformidade com a definição do esquema XML para o elemento **hashedAddresses**. 
    
5. O OSC chama **ISocialSession2::GetPeopleDetails**, fornecendo essa cadeia de caracteres XML de endereços com hash como o parâmetro _personAddresses_, para obter dinamicamente os detalhes atualizados das pessoas no parâmetro _personsCollection_. A cadeia de caracteres do parâmetro _personsCollection_ está em conformidade com a definição do esquema XML para o elemento **friends** no esquema XML. 

## <a name="parent-and-child-elements"></a>Elementos pai e filho

A seguir estão os dois elementos de nível superior no esquema **friends**. 
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**friends** <br/> |Representa o elemento raiz de uma lista de elementos **person**. O **ISocialPerson::GetFriendsAndColleagues**, o [ISocialSession::FindPerson](isocialsession-findperson.md) e o **ISocialSession2::GetPeopleDetails** retornam as cadeias de caracteres XML que estejam em conformidade com a definição de esquema do elemento **friends**.  <br/> |
|**person** <br/> |Representa uma pessoa em uma lista de elementos **person**. O método [ISocialPerson::GetDetails](isocialperson-getdetails.md) retorna uma cadeia de caracteres XML que está em conformidade com a definição de esquema do elemento **person**.  <br/> |
   
A tabela a seguir descreve cada elemento filho do elemento **person** no esquema XML do provedor OSC. 
  
Para obter uma definição completa do esquema XML do provedor OSC, inclusive de quais elementos são obrigatórios ou opcionais, confira o [Esquema XML do Provedor do Outlook Social Connector](outlook-social-connector-provider-xml-schema.md).
  
|**Elemento**|**Descrição**|
|:-----|:-----|
|**address** <br/> |Endereço físico da pessoa.  <br/> |
|**anniversary** <br/> |Data de aniversário de algum evento relacionado à pessoa.  <br/> |
|**askmeabout** <br/> |Tópicos de interesse ou especialização da pessoa.  <br/> |
|**birthday** <br/> |Data de nascimento da pessoa.  <br/> |
|**businessAddress** <br/> |Endereço físico do local de trabalho da pessoa.  <br/> |
|**businessCity** <br/> |Cidade do local de trabalho da pessoa.  <br/> |
|**businessCountryOrRegion** <br/> |País ou região do local de trabalho da pessoa.  <br/> |
|**businessState** <br/> |Estado ou província do local de trabalho da pessoa.  <br/> |
|**businessZip** <br/> |CEP ou código postal do local de trabalho da pessoa.  <br/> |
|**cell** <br/> |Número de telefone celular da pessoa.  <br/> |
|**city** <br/> |Cidade do endereço físico da pessoa.  <br/> |
|**company** <br/> |Nome da empresa associada à pessoa.  <br/> |
|**countryOrRegion** <br/> |País ou região do endereço físico da pessoa.  <br/> |
|**creationTime** <br/> |Hora da criação do perfil da pessoa na rede social.  <br/> |
|**emailAddress** <br/> |Endereço de email principal da pessoa.  <br/> |
|**emailAddress2** <br/> |Endereço de email secundário da pessoa.  <br/> |
|**emailAddress3** <br/> |Endereço de email terciário da pessoa.  <br/> |
|**expirationTime** <br/> |Hora que os dados do perfil da pessoa expiram na rede social.  <br/> |
|**fileAs** <br/> |Cadeia de caracteres pela qual a pessoa deve ser arquivada como um contato em um arquivo de contatos do Outlook.  <br/> |
|**firstName** <br/> |Primeiro nome da pessoa.  <br/> |
|**friendStatus** <br/> |Status de amigo dessa pessoa com o usuário conectado na rede social. Deve ser um dos seguintes valores: **friend**, **nonfriend**, **pending**, **pendingin**, **pendingout**.  <br/> |
|**fullName** <br/> |Nome completo da pessoa.  <br/> |
|**gender** <br/> |Gênero da pessoa. Deve ser um dos seguintes valores: **male**, **female**, **unspecified**.  <br/> |
|**homePhone** <br/> |Número de telefone residencial da pessoa.  <br/> |
|**index** <br/> |Localização do endereço com hash da pessoa no parâmetro de cadeia de caracteres _personsAddresses_ passado para uma chamada para o método **ISocialSession2::GetPeopleDetails**. Também indica o XML de **person** da pessoa na cadeia de caracteres _personsCollection_ retornada por **GetPeopleDetails**.  <br/> |
|**industries** <br/> |Setores com os quais a pessoa está envolvida.  <br/> |
|**interests** <br/> |Interesses ou hobbies da pessoa.  <br/> |
|**lastModificationTime** <br/> |Hora em que o perfil da pessoa foi modificado pela última vez na rede social.  <br/> |
|**lastName** <br/> |Sobrenome da pessoa.  <br/> |
|**location** <br/> |A localização da pessoa.  <br/> |
|**nickname** <br/> |Um nome mais curto ou nome inventado para a pessoa.  <br/> |
|**otherAddress** <br/> |Endereço alternativo da pessoa.  <br/> |
|**otherCity** <br/> |Cidade do endereço alternativo da pessoa.  <br/> |
|**otherCountryOrRegion** <br/> |País ou região do endereço alternativo da pessoa.  <br/> |
|**otherState** <br/> |Estado ou província do endereço alternativo da pessoa.  <br/> |
|**otherZip** <br/> |CEP ou código postal do endereço alternativo da pessoa.  <br/> |
|**phone** <br/> |Número de telefone principal de contato da pessoa.  <br/> |
|**pictureUrl** <br/> |URL da foto de perfil da pessoa.  <br/> |
|**relationship** <br/> |Relacionamento dessa pessoa com o usuário conectado.  <br/> |
|**schools** <br/> |Escolas/faculdades que a pessoa frequentou ou frequenta.  <br/> |
|**skills** <br/> |Habilidades da pessoa.  <br/> |
|**state** <br/> |Estado ou província do endereço físico da pessoa.  <br/> |
|**title** <br/> |Designação de título atribuído ao nome pessoa.  <br/> |
|**userID** <br/> |ID para identificar a pessoa na rede social.  <br/> |
|**webProfilePage** <br/> |Endereço da página da Web que contém o perfil da pessoa.  <br/> |
|**website** <br/> |Site da pessoa.  <br/> |
|**workPhone** <br/> |Número de telefone comercial da pessoa.  <br/> |
|**zip** <br/> |CEP ou código postal do endereço físico da pessoa.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Exemplo de XML de amigos](friends-xml-example.md)  
- [Sincronizar amigos e atividades](synchronizing-friends-and-activities.md)  
- [XML para recursos](xml-for-capabilities.md) 
- [XML para atividades](xml-for-activities.md)
- [Como desenvolver um provedor com o esquema XML do OSC](developing-a-provider-with-the-osc-xml-schema.md)

