    ServletContextHandler context = new ServletContextHandler();
        context.setContextPath("/");
        context.addServlet(new ServletHolder(new StoryServlet()), "/*");
        
        server.setHandler(context);
        server.start();
        server.join();
    }

    public static class StoryServlet extends HttpServlet {
        @Override
        protected void doGet(HttpServletRequest req, HttpServletResponse resp) 
                throws ServletException, IOException {
            
            resp.setContentType("text/html;charset=UTF-8");
            PrintWriter out = resp.getWriter();

            String authorName = "Adinath";
            String storyTitle = "The Iron Coffin";
            String instagramHandle = "adinath_prakashan";
            
            String storyContent = "<p>I remember those joyful streets, the laughter of friends, the warmth of family dinners. "
                    + "When the world got defeated, so did my purpose.</p>"
                    + "<p>A coward's life — I defined myself in just three words.</p>"
                    + "<p>When I had my first kid, I swore to protect her from anything, but when the time came, I left them for my own good. "
                    + "I could have saved them, but I didn't risk it.</p>"
                    + "<p>I prayed to God — let them be eaten, not me. I prayed hard. When finally death struck my family, I laughed. "
                    + "I laughed when my family's blood sprayed all over. I laughed at their desperate weeping. I remember me back then.</p>"
                    + "<p>Then I found a good old bunker. I'll live my life here — I thought. It was a paradise for a fucked-up world.</p>"
                    + "<p>I had that place all for me. All I had to do was to kill a man and his pregnant wife.</p>"
                    + "<p>Three years I lived in that paradise. Then I finally got the guts to go out. But I had a question in my mind — "
                    + "living for the lost memories gives you purpose, but does it lower your value?</p>"
                    + "<p>Three years I hid myself to find guilt that I never had. I never cared about any of them.</p>"
                    + "<p>Am I real? I thought to myself. A sadistic person who is self-absorbed — but isn't that the life every man led?</p>"
                    + "<p>I made a wishlist, for the day I get to step out of this bunker.</p>"
                    + "<p>The first thing I had on that list: video games —</p>"
                    + "<p>I could always see the smile other kids had when I walked past the arcade games. I wouldn't mind playing Pac-Man in those.</p>"
                    + "<p>Second, I wanted to swim against the river flow, but never even saw any once I left my hometown for studies.</p>"
                    + "<p>Those computers at my office had those river pictures — I remember planning a trip, but I don't know what stopped me.</p>"
                    + "<p>Does rain have the same smell as before? Or did it get ruined with blood?</p>"
                    + "<p>I want to run as fast as I can. I could have run with my children — but I killed them, didn't I?</p>"
                    + "<p>I was too scared to see the sunlight, and I hid in the dark. I survived this long because of my fear. "
                    + "I will be able to see all these things I desired every day of my life after this outbreak.</p>"
                    + "<p>I could sense no fear in me. I wish it had happened sooner, but I had the resources I needed. "
                    + "These few minutes are choking me. It's getting hard to breathe now. Maybe because I'm thrilled to see the day, "
                    + "or is it something else?</p>"
                    + "<p>Open it, coward — my mind said. And again.</p>"
                    + "<p>Open your eyes and see it for yourself.</p>"
                    + "<p>Did I open my eyes?</p>"
                    + "<p>I hid in this big room with nothing but food past these years. My loneliness became my only friend, "
                    + "a small flicker of life in this desolate place. Today was the day it ended. The swarm of those zombies gave me company. "
                    + "It was exhausting, but something I never got for quite some time. Now I got no strength to wake up. "
                    + "I wished those creatures had left me a leg so that I could see the sunlight once again, but I think I am just unlucky.</p>"
                    + "<p>I didn't know time moved this fast inside this room. I had many things yet to be done, but it's too late to think about it now. "
                    + "I am losing my vision. I guess I belonged in the dark from the very beginning itself. For the last time, "
                    + "I want to remember the life I had before. I want to see my children again, and now I know that I am much worse than those zombies. "
                    + "Those kids needed a father but got a selfish prick. I hid myself in this dirty bunker for that — just food and nothing else. "
                    + "Now I remember that day, packing my bag with my family for the trip to that river at my hometown. They were happy, "
                    + "and they raced to the car, and I lost. I was the last one to get to the car. The swarm of the zombies were faster. "
                    + "I was shocked at first. I couldn't imagine watching my life getting devoured in front of me. They screamed for me — "
                    + "but what did I do? It's — it's all in my head now. I ran away from them, didn't I? Did I really laugh, or did I cry?</p>"
                    + "<p>The bunker. I'll miss the day I first met you. A rotting man welcomed me inside, and his wife — "
                    + "her baby waving at me from her torn belly. Did I wave back, or did I kill them?</p>"
                    + "<p>My final breath is near. I will die alone in the grave I found years ago, with no hands to wipe "
                    + "my own tears and no legs to walk towards the light. The last thing I had on my list is to hold a mirror, "
                    + "to witness the villain of my own story's death.</p>";

            out.println("<!DOCTYPE html>");
            out.println("<html lang='en'>");
            out.println("<head>");
            out.println("    <meta charset='UTF-8'>");
            out.println("    <meta name='viewport' content='width=device-width, initial-scale=1.0'>");
            out.println("    <title>" + storyTitle + " | " + authorName + "</title>");
            out.println("    <style>");
            out.println("        :root {");
            out.println("            --primary: #1a1a2e;");
            out.println("            --secondary: #16213e;");
            out.println("            --accent: #0f3460;");
            out.println("            --text: #e6e6e6;");
            out.println("            --highlight: #e94560;");
            out.println("            --dark-text: #333;");
            out.println("        }");
            out.println("        * {");
            out.println("            box-sizing: border-box;");
            out.println("            margin: 0;");
            out.println("            padding: 0;");
            out.println("        }");
            out.println("        body {");
            out.println("            font-family: 'Cormorant Garamond', Georgia, serif;");
            out.println("            line-height: 1.8;");
            out.println("            color: var(--text);");
            out.println("            background-color: var(--primary);");
            out.println("            margin: 0;");
            out.println("            padding: 0;");
            out.println("            display: flex;");
            out.println("            flex-direction: column;");
            out.println("            min-height: 100vh;");
            out.println("            background-image: linear-gradient(to bottom, var(--primary), url('data:image/svg+xml;utf8,<svg xmlns=\"http://www.w3.org/2000/svg\" width=\"100\" height=\"100\" viewBox=\"0 0 100 100\"><rect fill=\"%230f3460\" width=\"50\" height=\"50\" x=\"0\" y=\"0\"></rect><rect fill=\"%230f3460\" width=\"50\" height=\"50\" x=\"50\" y=\"50\"></rect></svg>');");
            out.println("            background-size: 10px 10px;");
            out.println("        }");
            out.println("        .container {");
            out.println("            max-width: 800px;");
            out.println("            margin: 0 auto;");
            out.println("            padding: 2rem;");
            out.println("            flex: 1;");
            out.println("        }");
            out.println("        header {");
            out.println("            text-align: center;");
            out.println("            margin-bottom: 3rem;");
            out.println("            border-bottom: 1px solid var(--accent);");
            out.println("            padding-bottom: 2rem;");
            out.println("            position: relative;");
            out.println("        }");
            out.println("        header::after {");
            out.println("            content: '';");
            out.println("            position: absolute;");
            out.println("            bottom: -5px;");
            out.println("            left: 25%;");
            out.println("            width: 50%;");
            out.println("            height: 1px;");
            out.println("            background: var(--highlight);");
            out.println("        }");
            out.println("        h1 {");
            out.println("            color: var(--highlight);");
            out.println("            font-size: 2.8rem;");
            out.println("            margin-bottom: 0.5rem;");
            out.println("            font-weight: 700;");
            out.println("            letter-spacing: 1px;");
            out.println("            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);");
            out.println("        }");
            out.println("        .author-intro {");
            out.println("            font-style: italic;");
            out.println("            margin: 2rem 0;");
            out.println("            padding: 1rem;");
            out.println("            background-color: rgba(15, 52, 96, 0.3);");
            out.println("            border-left: 3px solid var(--highlight);");
            out.println("        }");
            out.println("        .story-content {");
            out.println("            font-size: 1.15rem;");
            out.println("            text-align: justify;");
            out.println("            margin-bottom: 3rem;");
            out.println("        }");
            out.println("        .story-content p {");
            out.println("            margin-bottom: 1.5rem;");
            out.println("            text-indent: 1.5em;");
            out.println("        }");
            out.println("        .story-content p:first-of-type {");
            out.println("            text-indent: 0;");
            out.println("            font-weight: bold;");
            out.println("        }");
            out.println("        .story-content p:last-of-type {");
            out.println("            margin-bottom: 0;");
            out.println("            font-style: italic;");
            out.println("        }");
            out.println("        .social {");
            out.println("            text-align: center;");
            out.println("            margin: 3rem 0;");
            out.println("        }");
            out.println("        .instagram-btn {");
            out.println("            display: inline-flex;");
            out.println("            align-items: center;");
            out.println("            justify-content: center;");
            out.println("            background: linear-gradient(45deg, #405de6, #5851db, #833ab4, #c13584, #e1306c, #fd1d1d);");
            out.println("            color: white !important;");
            out.println("            padding: 0.8rem 1.8rem;");
            out.println("            border-radius: 25px;");
            out.println("            text-decoration: none;");
            out.println("            font-weight: bold;");
            out.println("            transition: all 0.3s ease;");
            out.println("            border: none;");
            out.println("            cursor: pointer;");
            out.println("            font-size: 1rem;");
            out.println("            box-shadow: 0 4px 6px rgba(0,0,0,0.1);");
            out.println("        }");
            out.println("        .instagram-btn:hover {");
            out.println("            transform: translateY(-3px);");
            out.println("            box-shadow: 0 6px 8px rgba(0,0,0,0.15);");
            out.println("        }");
            out.println("        .instagram-btn:active {");
            out.println("            transform: translateY(1px);");
            out.println("        }");
            out.println("        .instagram-icon {");
            out.println("            margin-right: 8px;");
            out.println("            font-size: 1.2rem;");
            out.println("        }");
            out.println("        footer {");
            out.println("            text-align: center;");
            out.println("            padding: 1.5rem;");
            out.println("            background-color: var(--secondary);");
            out.println("            margin-top: 3rem;");
            out.println("            font-size: 0.9rem;");
            out.println("        }");
            out.println("        @media (max-width: 768px) {");
            out.println("            .container {");
            out.println("                padding: 1.5rem;");
            out.println("            }");
            out.println("            h1 {");
            out.println("                font-size: 2.2rem;");
            out.println("            }");
            out.println("            .story-content {");
            out.println("                font-size: 1.05rem;");
            out.println("                text-align: left;");
            out.println("            }");
            out.println("        }");
            out.println("        @media (max-width: 480px) {");
            out.println("            h1 {");
            out.println("                font-size: 1.8rem;");
            out.println("            }");
            out.println("            .container {");
            out.println("                padding: 1rem;");
            out.println("            }");
            out.println("        }");
            out.println("        /* Fade-in animation */");
            out.println("        @keyframes fadeIn {");
            out.println("            from { opacity: 0; transform: translateY(20px); }");
            out.println("            to { opacity: 1; transform: translateY(0); }");
            out.println("        }");
            out.println("        .animated-entry {");
            out.println("            animation: fadeIn 1s ease-out forwards;");
            out.println("        }");
            out.println("        .delay-1 { animation-delay: 0.3s; }");
            out.println("        .delay-2 { animation-delay: 0.6s; }");
            out.println("        .delay-3 { animation-delay: 0.9s; }");
            out.println("    </style>");
            out.println("    <link href='https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&display=swap' rel='stylesheet'>");
            out.println("    <link rel='stylesheet' href='https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css'>");
            out.println("</head>");
            out.println("<body>");
            out.println("    <div class='container'>");
            out.println("        <header class='animated-entry'>");
            out.println("            <h1>" + storyTitle + "</h1>");
            out.println("            <div class='author-intro delay-1'>");
            out.println("                <p>Hey, my name's " + Adinath prakashan + ", and I'm a writer. I've spent over a year working on a book — still working on it.</p>");
            out.println("                <p>Below is a short monologue-style story. I wrote it to showcase what I can do.</p>");
            out.println("                <p>If you love it — support me.<br>If you don't, forget I exist.</p>");
            out.println("            </div>");
            out.println("        </header>");
            out.println("        <div class='story-content delay-2'>" + storyContent + "</div>");
            out.println("        <div class='social delay-3'>");
            out.println("            <a href='https://instagram.com/" + adinath_prakashan + "' class='instagram-btn' target='_blank'>");
            out.println("                <i class='fab fa-instagram instagram-icon'></i>");
            out.println("                Follow @" + adinath_prakashan);
            out.println("            </a>");
            out.println("        </div>");
            out.println("    </div>");
            out.println("    <footer class='delay-3'>");
            out.println("        &copy; " + java.time.Year.now().getValue() + " " + Adinath prakashan+ ". All rights reserved.");
            out.println("    </footer>");
            out.println("    <script>");
            out.println("        // Instagram button hover effect");
            out.println("        const instaBtn = document.querySelector('.instagram-btn');");
            out.println("        const colors = [");
            out.println("            'linear-gradient(45deg, #405de6, #5851db, #833ab4, #c13584, #e1306c, #fd1d1d)',");
            out.println("            'linear-gradient(45deg, #fd1d1d, #e1306c, #c13584, #833ab4, #5851db, #405de6)'");
            out.println("        ];");
            out.println("        let currentColor = 0;");
            out.println("        ");
            out.println("        function changeColor() {");
            out.println("            currentColor = (currentColor + 1) % colors.length;");
            out.println("            instaBtn.style.background = colors[currentColor];");
            out.println("        }");
            out.println("        ");
            out.println("        instaBtn.addEventListener('mouseover', () => {");
            out.println("            changeColor();");
            out.println("            colorInterval = setInterval(changeColor, 1000);");
            out.println("        });");
            out.println("        ");
            out.println("        instaBtn.addEventListener('mouseout', () => {");
            out.println("            clearInterval(colorInterval);");
            out.println("            instaBtn.style.background = colors[0];");
            out.println("        });");
            out.println("        ");
            out.println("        // Scroll reveal animation");
            out.println("        const observer = new IntersectionObserver((entries) => {");
            out.println("            entries.forEach(entry => {");
            out.println("                if (entry.isIntersecting) {");
            out.println("                    entry.target.classList.add('animate');");
            out.println("                }");
            out.println("            });");
            out.println("     
