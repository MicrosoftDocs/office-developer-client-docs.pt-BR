---
title: Endereços únicos
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9224c694-b26f-42c7-9404-ee2dd832cfbb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 504ae8dddbddb1c7049574b1bdcc575a10a62c8f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570090"
---
# <a name="one-off-addresses"></a>Endereços únicos

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Endereços únicos são usados para enviar mensagens para destinatários únicos, destinatários que não têm uma entrada correspondente em qualquer um dos contêineres de catálogo de endereços da sessão. Os clientes podem criar endereços únicos quando adicionam novas entradas para o catálogo de endereços ou novos destinatários à lista de destinatários de uma mensagem de saída. Endereços únicos podem ser adicionados para qualquer contêiner que pode ser modificado.
  
Para criar um endereço único, clientes usam um modelo especial que contém os controles de edição para inserir todas as informações que constitui um endereço one-off. Endereços únicos, como os endereços de outros tipos de usam um formato predefinido. O formato de endereço one-off é definido por MAPI da seguinte maneira:
  
`Display name[Address type:Email address]`
  
Há seis componentes neste formato e algumas regras sobre orçar caracteres. Os componentes são descritos na tabela a seguir.
  
|**Componente**|**Uso**|**Descrição**|
|:-----|:-----|:-----|
|Nome para exibição  <br/> |Opcional  <br/> |Se não estiver presente, o **IAddrBook::ResolveName** usa na parte visível do endereço de email como o nome para exibição. Podem incluir espaços em branco. Para obter mais informações, consulte [IAddrBook::ResolveName](iaddrbook-resolvename.md).  <br/> |
|[  <br/> |Obrigatório  <br/> |Delineia o início das informações do tipo e o endereço.  <br/> |
|]  <br/> |Obrigatório  <br/> |Delineia o final das informações do tipo e o endereço. Se qualquer coisa diferente de espaço em branco segue esse caractere, a entrada não é tratada como um destinatário personalizado.  <br/> |
|Tipo de endereço  <br/> |Obrigatório  <br/> |Tipo de endereço; mapas para um formato de endereço específica. Para obter mais informações, consulte [Tipos de endereço de MAPI](mapi-address-types.md).  <br/> |
|:  <br/> |Obrigatório  <br/> |Separa o tipo de endereço do endereço de email.  <br/> |
|Endereço de email  <br/> |Obrigatório  <br/> |Endereço do destinatário. Podem incluir espaços em branco.  <br/> |
   
O MAPI usa determinados conjuntos de caracteres de cotação para permitir que os endereços conter caracteres especiais, como vírgula (,), colchete esquerdo ([), e dois-pontos (:) e alguns caracteres untypeable como o carro retornam ou feed ou qualquer outro equivalente hexadecimal de linha. O caractere de cotação é a barra invertida (\). Portanto, se os clientes ou provedores devem inserir uma barra invertida em um endereço, eles devem precedê-lo com o caractere de cotação ("\\").
  
Clientes e provedores de serviços podem usar essa técnica de cotação em qualquer um dos campos nonfixed, digitável. Por exemplo, a seguinte entrada converte para Bill Lee como o nome de exibição, MSPEER como o tipo de endereço, e \\billll\in como o endereço de email:
  
`Bill Lee[MSPEER:\\\\billl\in]`

Para inserir caracteres especiais nontypeable, clientes e provedores de serviços usam um caractere de cotação seguido por um x e dois dígitos hexadecimais para representar seus equivalentes hexadecimais. Por exemplo, se um endereço tiver um caractere de nontypeable que é igual a um carro retornar, (\0d) em hexadecimal, um cliente digitaria-las como:
  
`Fax Recipient[fax:recipient\x0dbuilding\x0doffice\x0d555-1212\x0d]`

**IAddrBook::ResolveName** analisa também automaticamente a maioria dos endereços de SMTP, procurando endereços com o seguinte formato: 
  
`XXX@YYY.ZZZ`

Embora nem todos os formatos RFC822 possíveis são tratados, essa análise automática é adequado para a maioria dos usuários. **ResolveName** inclui essa funcionalidade para permitir que os usuários insiram endereços SMTP diretamente em uma mensagem e ter essa mensagem vá para o usuário da Internet. Os componentes XXX, YYY e ZZZ do endereço podem ser um ou mais caracteres. O sinal de arroba (@) não podem ser incluídos no endereço XXX, YYY ou ZZZ componentes e o componente YYY também não podem incluir o período. Como os seguintes caracteres são caracteres especiais em endereços SMTP, MAPI converte automaticamente um nome de exibição que contém esses caracteres em um endereço único: 
  
- \>\>
    
- @
    
- \<\>
    
- .
    
Cada endereço one-off é atribuído a um identificador de entrada únicos correspondente. Para tornar essa atribuição, ligue para clientes **IAddrBook::CreateOneOff** e provedores de transporte chamarem **IMAPISupport::CreateOneOff**. Para obter mais informações, consulte [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) e [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md). Durante o processamento de mensagens de entrada, provedores de transporte criar identificadores de entrada únicos para os endereços de gateway e para endereços que não podem ser manipulados pelos provedores de catálogo de endereços associado do transporte. Provedores de transporte verificam o tipo de cada endereço em uma mensagem para determinar se ele pode ser tratado por um fornecedor de catálogo de endereços associado com o transporte. Se não for possível, provedores de transporte chamarem **IMAPISupport::CreateOneOff** para associar o endereço com um identificador de entrada únicos. 
  
Identificadores de entrada únicos incluem as seguintes informações na seguinte ordem:
  
1. **MAPIUID**
    
2. Versão
    
3. Sinalizadores
    
4. Nome para exibição
    
5. Tipo de endereço
    
6. Endereço de email
    
Nas chamadas **IAddrBook::CreateOneOff** e **IMAPISupport::CreateOneOff**, clientes e provedores de transporte podem definir um sinalizador que indica se ou não o destinatário representado pelo endereço único pode processar texto formatado ou incorporados OLE objetos. Para indicar que um destinatário pode manipular texto formatado e objetos OLE, clientes e o conjunto de provedores de transporte o sinalizador MAPI_SEND_NO_RICH_INFO no parâmetro _ulFlags_ . MAPI, em seguida, define a propriedade de **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) do destinatário únicos como FALSE. Quando esse sinalizador não estiver definida, o MAPI define **PR_SEND_RICH_INFO** como TRUE, a menos que o endereço único será interpretado como um endereço SMTP. Neste caso um, **PR_SEND_RICH_INFO** padrão é FALSE. 
  
## <a name="see-also"></a>Confira também

- [IAddrBook::ResolveName](iaddrbook-resolvename.md)

