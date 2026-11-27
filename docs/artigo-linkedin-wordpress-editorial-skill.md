# Como transformei uma rotina editorial em um produto de IA para WordPress

Eu terminava de escrever um artigo e ainda tinha uma segunda tarefa pela frente. Precisava levar o texto ao WordPress, conferir o título, ajustar o endereço da página e procurar um rascunho que talvez já estivesse lá. Eram passos pequenos. Como eu os repetia a cada artigo, conhecia bem o trabalho que queria automatizar e o ponto em que queria retomar o controle.

Foi dessa rotina que surgiu a **WordPress Editorial Skill**, um produto que transforma um artigo pronto em um rascunho verificável. Entre a primeira ferramenta e o lançamento, aprendi a prestar atenção em duas coisas que parecem óbvias até que uma automação precise lidar com elas. Como sei que o sistema gravou o que eu pedi? O que acontece se eu enviar o mesmo artigo de novo?

## A integração veio primeiro

Comecei pelo **WordPress MCP Publisher**. Ele oferece ferramentas para que um assistente consulte posts e grave rascunhos pela API do WordPress. Usei o Model Context Protocol, ou MCP, para expor essas operações a clientes compatíveis e publiquei o código no GitHub sob licença MIT.

A Agensi encontrou o Publisher ao pesquisar projetos MCP relacionados à publicação no WordPress. A conversa me fez olhar para o que havia construído do ponto de vista de alguém que precisaria instalar e usar aquilo pela primeira vez. Consultar e gravar posts já era possível. O trabalho seguinte era definir como essas operações deveriam ser usadas na preparação de um artigo.

## A ordem das decisões virou parte do produto

Antes de gravar, eu queria que o assistente confirmasse em qual site estava operando. Também queria que procurasse um post correspondente pelo título ou pelo *slug*, o trecho da URL que identifica a página. Depois da gravação, a tarefa só estaria concluída quando fosse possível localizar o rascunho e conferir o que havia sido salvo. A publicação ficaria com o editor.

Foi aí que os dois projetos ganharam papéis claros. O Publisher fornece as operações. A Skill orienta o assistente sobre a ordem em que deve usá-las e o que fazer quando encontra uma duplicata. Mantive a integração em um projeto independente e trabalhei na Skill como o produto que reúne as decisões desse fluxo editorial.

## O segundo envio foi o teste decisivo

Comecei os testes em uma instalação local do WordPress. Depois rodei o fluxo completo no Codex desktop, conectado a um ambiente de homologação. O assistente criou um rascunho e consultou o WordPress para conferir o status, o endereço e o conteúdo gravado.

Em seguida, enviei o mesmo artigo outra vez. As buscas por título e *slug* encontraram o rascunho existente e o fluxo encerrou antes de uma segunda gravação. Esse foi o resultado que eu precisava ver para o meu uso diário. Eu podia retomar um artigo e encontrar o trabalho que já estava no painel. O teste cobriu reenvios sucessivos. Envios simultâneos ficaram fora dessa validação.

Fazer essa distinção mudou a forma como penso em automação. Uma resposta de sucesso é fácil de exibir. O que me deu confiança para usar o fluxo foi conseguir abrir o WordPress, localizar o post pelo ID e verificar por conta própria o que tinha acontecido.

## O que levei do lançamento

A **WordPress Editorial Skill** foi aprovada e disponibilizada na Agensi. O lançamento reuniu duas partes da minha trajetória que sempre andaram juntas. Como criador de conteúdo, eu conhecia os detalhes da rotina editorial. Como profissional de tecnologia, pude transformar essa rotina em uma integração, definir um escopo e testar o comportamento em situações que realmente acontecem durante o trabalho.

Para mim, a entrega está naquele momento em que posso voltar ao WordPress e continuar de onde parei. O texto está salvo como rascunho, eu consigo verificar o que foi gravado e a decisão de publicar continua comigo.

[Conheça a WordPress Editorial Skill na Agensi](https://www.agensi.io/skills/wordpress-editorial-skill).
