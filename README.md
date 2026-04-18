import { motion } from "framer-motion";
import { Card, CardContent } from "@/components/ui/card";
import { Badge } from "@/components/ui/badge";
import { Button } from "@/components/ui/button";

const GITHUB_URL = "https://github.com/YOUR_GITHUB_USERNAME";
const EMAIL = "alona.lavi@weizmann.ac.il";

const fadeUp = {
  hidden: { opacity: 0, y: 24 },
  visible: { opacity: 1, y: 0 },
};

function IconWrapper({ children, className = "h-5 w-5" }) {
  return <span className={className}>{children}</span>;
}

function MailIcon({ className = "h-5 w-5" }) {
  return (
    <IconWrapper className={className}>
      <svg viewBox="0 0 24 24" fill="none" className="h-full w-full" xmlns="http://www.w3.org/2000/svg">
        <path d="M4 6.75h16v10.5H4V6.75Z" stroke="currentColor" strokeWidth="1.8" rx="2" />
        <path d="m5 8 7 5 7-5" stroke="currentColor" strokeWidth="1.8" strokeLinecap="round" strokeLinejoin="round" />
      </svg>
    </IconWrapper>
  );
}

function GitHubIcon({ className = "h-5 w-5" }) {
  return (
    <IconWrapper className={className}>
      <svg viewBox="0 0 24 24" fill="none" className="h-full w-full" xmlns="http://www.w3.org/2000/svg">
        <path
          d="M12 3.75a8.25 8.25 0 0 0-2.61 16.08c.41.08.56-.18.56-.4v-1.42c-2.28.5-2.76-.97-2.76-.97-.37-.93-.91-1.18-.91-1.18-.74-.5.06-.49.06-.49.82.06 1.25.84 1.25.84.73 1.25 1.91.89 2.38.68.07-.53.29-.89.52-1.09-1.82-.21-3.73-.91-3.73-4.04 0-.89.32-1.62.84-2.19-.08-.21-.36-1.06.08-2.21 0 0 .69-.22 2.27.84A7.9 7.9 0 0 1 12 7.8c.7 0 1.41.09 2.07.27 1.58-1.06 2.27-.84 2.27-.84.44 1.15.16 2 .08 2.21.52.57.84 1.3.84 2.19 0 3.14-1.92 3.82-3.75 4.03.3.26.56.76.56 1.54v2.28c0 .22.15.49.57.4A8.25 8.25 0 0 0 12 3.75Z"
          stroke="currentColor"
          strokeWidth="1.2"
          strokeLinejoin="round"
        />
      </svg>
    </IconWrapper>
  );
}

function MicroscopeIcon({ className = "h-5 w-5" }) {
  return (
    <IconWrapper className={className}>
      <svg viewBox="0 0 24 24" fill="none" className="h-full w-full" xmlns="http://www.w3.org/2000/svg">
        <path d="M10 4.5h3.5" stroke="currentColor" strokeWidth="1.8" strokeLinecap="round" />
        <path d="m12.5 4.5 1.75 4.25" stroke="currentColor" strokeWidth="1.8" strokeLinecap="round" />
        <path d="m10.5 8.25 4.25-1.75" stroke="currentColor" strokeWidth="1.8" strokeLinecap="round" />
        <path d="M8.75 13.25a4 4 0 1 0 5.66 5.66" stroke="currentColor" strokeWidth="1.8" strokeLinecap="round" />
        <path d="M13.5 10.5 9.75 14.25" stroke="currentColor" strokeWidth="1.8" strokeLinecap="round" />
        <path d="M5 20h14" stroke="currentColor" strokeWidth="1.8" strokeLinecap="round" />
      </svg>
    </IconWrapper>
  );
}

function DnaIcon({ className = "h-5 w-5" }) {
  return (
    <IconWrapper className={className}>
      <svg viewBox="0 0 24 24" fill="none" className="h-full w-full" xmlns="http://www.w3.org/2000/svg">
        <path d="M8 4c0 4 8 4 8 8s-8 4-8 8" stroke="currentColor" strokeWidth="1.8" strokeLinecap="round" />
        <path d="M16 4c0 4-8 4-8 8s8 4 8 8" stroke="currentColor" strokeWidth="1.8" strokeLinecap="round" />
        <path d="M9 6h6M8 12h8m-7 6h6" stroke="currentColor" strokeWidth="1.8" strokeLinecap="round" />
      </svg>
    </IconWrapper>
  );
}

function CodeIcon({ className = "h-5 w-5" }) {
  return (
    <IconWrapper className={className}>
      <svg viewBox="0 0 24 24" fill="none" className="h-full w-full" xmlns="http://www.w3.org/2000/svg">
        <path d="m8 8-4 4 4 4M16 8l4 4-4 4M13.5 5.5 10.5 18.5" stroke="currentColor" strokeWidth="1.8" strokeLinecap="round" strokeLinejoin="round" />
      </svg>
    </IconWrapper>
  );
}

function BookIcon({ className = "h-5 w-5" }) {
  return (
    <IconWrapper className={className}>
      <svg viewBox="0 0 24 24" fill="none" className="h-full w-full" xmlns="http://www.w3.org/2000/svg">
        <path d="M6.5 5.5h8a3 3 0 0 1 3 3v9h-8a3 3 0 0 0-3 3v-15Z" stroke="currentColor" strokeWidth="1.8" strokeLinejoin="round" />
        <path d="M6.5 5.5a2.5 2.5 0 0 0-2.5 2.5v11.5a2.5 2.5 0 0 1 2.5-2.5h11" stroke="currentColor" strokeWidth="1.8" strokeLinejoin="round" />
      </svg>
    </IconWrapper>
  );
}

function ActivityIcon({ className = "h-5 w-5" }) {
  return (
    <IconWrapper className={className}>
      <svg viewBox="0 0 24 24" fill="none" className="h-full w-full" xmlns="http://www.w3.org/2000/svg">
        <path d="M3 12h4l2.2-4.5L13 17l2.4-5H21" stroke="currentColor" strokeWidth="1.8" strokeLinecap="round" strokeLinejoin="round" />
      </svg>
    </IconWrapper>
  );
}

function SparklesIcon({ className = "h-5 w-5" }) {
  return (
    <IconWrapper className={className}>
      <svg viewBox="0 0 24 24" fill="none" className="h-full w-full" xmlns="http://www.w3.org/2000/svg">
        <path d="M12 3.5 13.7 8l4.8 1.8-4.8 1.7L12 16l-1.7-4.5L5.5 9.8 10.3 8 12 3.5ZM18.5 15l.8 2.2 2.2.8-2.2.8-.8 2.2-.8-2.2-2.2-.8 2.2-.8.8-2.2ZM5.5 14l1.1 2.9 2.9 1.1-2.9 1.1-1.1 2.9-1.1-2.9L1.5 18l2.9-1.1L5.5 14Z" stroke="currentColor" strokeWidth="1.4" strokeLinejoin="round" />
      </svg>
    </IconWrapper>
  );
}

function ChevronRightIcon({ className = "h-4 w-4" }) {
  return (
    <IconWrapper className={className}>
      <svg viewBox="0 0 24 24" fill="none" className="h-full w-full" xmlns="http://www.w3.org/2000/svg">
        <path d="m9 6 6 6-6 6" stroke="currentColor" strokeWidth="1.8" strokeLinecap="round" strokeLinejoin="round" />
      </svg>
    </IconWrapper>
  );
}

function SectionTitle({ eyebrow, title, description }) {
  return (
    <div className="max-w-3xl">
      <p className="mb-3 text-sm font-medium uppercase tracking-[0.25em] text-slate-500">
        {eyebrow}
      </p>
      <h2 className="text-3xl font-semibold tracking-tight text-slate-900 sm:text-4xl">
        {title}
      </h2>
      {description ? (
        <p className="mt-4 text-base leading-7 text-slate-600 sm:text-lg">
          {description}
        </p>
      ) : null}
    </div>
  );
}

function BackgroundPattern() {
  return (
    <div className="pointer-events-none absolute inset-0 overflow-hidden">
      <div className="absolute inset-0 bg-[linear-gradient(to_right,rgba(15,23,42,0.05)_1px,transparent_1px),linear-gradient(to_bottom,rgba(15,23,42,0.05)_1px,transparent_1px)] bg-[size:48px_48px]" />
      <div className="absolute left-1/2 top-[-10rem] h-[28rem] w-[28rem] -translate-x-1/2 rounded-full bg-cyan-200/35 blur-3xl" />
      <div className="absolute bottom-[-8rem] right-[-6rem] h-[22rem] w-[22rem] rounded-full bg-indigo-200/35 blur-3xl" />
      <div className="absolute left-[-5rem] top-[40%] h-[18rem] w-[18rem] rounded-full bg-emerald-200/20 blur-3xl" />
    </div>
  );
}

function ScientificGraphic() {
  return (
    <div className="relative mx-auto flex h-[320px] w-full max-w-[520px] items-center justify-center sm:h-[380px]">
      <div className="absolute inset-0 rounded-[2rem] border border-white/70 bg-white/55 shadow-[0_20px_70px_rgba(15,23,42,0.12)] backdrop-blur-xl" />
      <svg
        viewBox="0 0 600 420"
        className="relative h-full w-full p-6"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <defs>
          <linearGradient id="lineGradient" x1="80" y1="40" x2="520" y2="360" gradientUnits="userSpaceOnUse">
            <stop stopColor="#0f172a" stopOpacity="0.9" />
            <stop offset="0.5" stopColor="#0f766e" stopOpacity="0.8" />
            <stop offset="1" stopColor="#2563eb" stopOpacity="0.8" />
          </linearGradient>
          <linearGradient id="softGradient" x1="120" y1="60" x2="520" y2="320" gradientUnits="userSpaceOnUse">
            <stop stopColor="#22d3ee" stopOpacity="0.22" />
            <stop offset="1" stopColor="#818cf8" stopOpacity="0.12" />
          </linearGradient>
        </defs>

        <rect x="56" y="48" width="488" height="324" rx="24" fill="url(#softGradient)" />
        <path d="M170 80C275 135 325 285 430 340" stroke="url(#lineGradient)" strokeWidth="4" strokeLinecap="round" />
        <path d="M430 80C325 135 275 285 170 340" stroke="url(#lineGradient)" strokeWidth="4" strokeLinecap="round" />

        {[110, 145, 180, 215, 250, 285, 320].map((y, i) => (
          <g key={y} opacity="0.9">
            <path
              d={`M${190 + i * 7} ${y} C 255 ${y + 18}, 345 ${y - 18}, ${410 - i * 7} ${y + 6}`}
              stroke="#0f172a"
              strokeOpacity="0.18"
              strokeWidth="2"
            />
            <circle cx={220 + i * 18} cy={y + 6} r="4.5" fill="#0f766e" fillOpacity="0.85" />
            <circle cx={375 - i * 15} cy={y - 2} r="4.5" fill="#2563eb" fillOpacity="0.8" />
          </g>
        ))}

        {[
          [145, 110], [220, 95], [310, 130], [385, 105], [460, 145],
          [170, 255], [245, 225], [330, 255], [415, 230], [485, 280],
        ].map(([cx, cy], idx) => (
          <g key={idx}>
            <circle cx={cx} cy={cy} r="6" fill="#0f172a" fillOpacity="0.85" />
            <circle cx={cx} cy={cy} r="16" fill="#0f172a" fillOpacity="0.06" />
          </g>
        ))}

        <path d="M126 310H504" stroke="#0f172a" strokeOpacity="0.12" strokeWidth="2" strokeDasharray="7 8" />
        <path d="M126 160H260" stroke="#0f172a" strokeOpacity="0.1" strokeWidth="2" strokeDasharray="7 8" />

        <rect x="95" y="85" width="96" height="34" rx="17" fill="#ffffff" fillOpacity="0.88" />
        <text x="143" y="106" textAnchor="middle" fill="#0f172a" fontSize="13" fontWeight="600">
          Epigenetics
        </text>

        <rect x="392" y="298" width="115" height="34" rx="17" fill="#ffffff" fillOpacity="0.88" />
        <text x="450" y="319" textAnchor="middle" fill="#0f172a" fontSize="13" fontWeight="600">
          Genomic data
        </text>
      </svg>
    </div>
  );
}

const aboutCards = [
  {
    icon: MicroscopeIcon,
    title: "Wet-lab + computational",
    text: "My Master’s project combines experimental biology with computational analysis to study complex genomic systems from multiple angles.",
  },
  {
    icon: DnaIcon,
    title: "Epigenetic regulation",
    text: "I’m especially interested in how chromatin states, Polycomb-related mechanisms, and sequence features help organize developmental regulation.",
  },
  {
    icon: SparklesIcon,
    title: "Scientific curiosity",
    text: "I like projects that connect mechanism, data, and clear conceptual models rather than just generating results in isolation.",
  },
];

const sideCards = [
  {
    icon: ActivityIcon,
    title: "Analysis mindset",
    text: "I like structured data exploration, interpretable models, and clear reasoning from experiment to conclusion.",
  },
  {
    icon: BookIcon,
    title: "Scientific communication",
    text: "I care about presenting ideas clearly, whether in figures, code, talks, or writing meant for collaborators.",
  },
];

const hobbies = ["Reading", "Working out", "Long walks with my dog", "Cooking"];

export default function AlonaPersonalSite() {
  return (
    <main className="min-h-screen bg-slate-50 text-slate-900">
      <div className="relative isolate overflow-hidden">
        <BackgroundPattern />

        <section className="relative mx-auto max-w-7xl px-6 pb-20 pt-8 sm:px-8 lg:px-10 lg:pb-28 lg:pt-10">
          <motion.div
            initial="hidden"
            animate="visible"
            variants={fadeUp}
            transition={{ duration: 0.6 }}
            className="mb-10 flex items-center justify-between"
          >
            <div className="flex items-center gap-3">
              <div className="flex h-11 w-11 items-center justify-center rounded-2xl border border-slate-200 bg-white shadow-sm">
                <DnaIcon className="h-5 w-5" />
              </div>
              <div>
                <p className="text-sm font-semibold tracking-wide text-slate-900">Alona Lavi</p>
                <p className="text-sm text-slate-500">MSc student · Weizmann Institute of Science</p>
              </div>
            </div>

            <div className="hidden items-center gap-3 sm:flex">
              <Button asChild variant="outline" className="rounded-full bg-white/80 backdrop-blur">
                <a href={GITHUB_URL} target="_blank" rel="noreferrer">
                  <GitHubIcon className="mr-2 h-4 w-4" />
                  GitHub
                </a>
              </Button>
              <Button asChild className="rounded-full">
                <a href={`mailto:${EMAIL}`}>
                  <MailIcon className="mr-2 h-4 w-4" />
                  Contact
                </a>
              </Button>
            </div>
          </motion.div>

          <div className="grid items-center gap-12 lg:grid-cols-[1.2fr_0.9fr] lg:gap-16">
            <motion.div
              initial="hidden"
              animate="visible"
              variants={fadeUp}
              transition={{ duration: 0.7, delay: 0.05 }}
            >
              <Badge className="mb-5 rounded-full border border-cyan-200 bg-cyan-50 px-4 py-1.5 text-cyan-900 hover:bg-cyan-50">
                Molecular Biology · Epigenetics · Computational Biology
              </Badge>

              <h1 className="max-w-4xl text-4xl font-semibold tracking-tight text-slate-950 sm:text-5xl lg:text-6xl">
                Welcome to my personal page.
              </h1>

              <p className="mt-6 max-w-2xl text-lg leading-8 text-slate-600 sm:text-xl">
                I’m Alona Lavi, an MSc student at the Weizmann Institute of Science studying
                chromatin architecture, genomic sequence grammar, and the mechanisms that shape
                epigenetic regulation.
              </p>

              <div className="mt-8 flex flex-wrap gap-3">
                <Badge variant="secondary" className="rounded-full px-4 py-1.5 text-sm">Stelzer Lab</Badge>
                <Badge variant="secondary" className="rounded-full px-4 py-1.5 text-sm">Scientific computing</Badge>
                <Badge variant="secondary" className="rounded-full px-4 py-1.5 text-sm">Data-rich biology</Badge>
              </div>

              <div className="mt-10 flex flex-wrap gap-4">
                <Button asChild size="lg" className="rounded-full px-6">
                  <a href={`mailto:${EMAIL}`}>
                    Get in touch
                    <ChevronRightIcon className="ml-2 h-4 w-4" />
                  </a>
                </Button>
                <Button asChild size="lg" variant="outline" className="rounded-full border-slate-300 bg-white/80 px-6 backdrop-blur">
                  <a href={GITHUB_URL} target="_blank" rel="noreferrer">
                    View projects
                  </a>
                </Button>
              </div>
            </motion.div>

            <motion.div
              initial={{ opacity: 0, y: 20 }}
              animate={{ opacity: 1, y: 0 }}
              transition={{ duration: 0.7, delay: 0.15 }}
            >
              <ScientificGraphic />
            </motion.div>
          </div>
        </section>
      </div>

      <section className="mx-auto max-w-7xl px-6 py-20 sm:px-8 lg:px-10">
        <motion.div
          initial="hidden"
          whileInView="visible"
          viewport={{ once: true, amount: 0.2 }}
          variants={fadeUp}
          transition={{ duration: 0.5 }}
        >
          <SectionTitle
            eyebrow="About me"
            title="Researching how sequence and chromatin shape cell identity"
            description="I am a researcher in the Stelzer Lab. My academic work centers on molecular biology and epigenetics, with a specific focus on chromatin architecture and genomic sequence grammar."
          />
        </motion.div>

        <div className="mt-10 grid gap-6 lg:grid-cols-3">
          {aboutCards.map((item, index) => {
            const Icon = item.icon;
            return (
              <motion.div
                key={item.title}
                initial="hidden"
                whileInView="visible"
                viewport={{ once: true, amount: 0.2 }}
                variants={fadeUp}
                transition={{ duration: 0.45, delay: index * 0.08 }}
              >
                <Card className="h-full rounded-[1.75rem] border-slate-200/70 bg-white/80 shadow-[0_10px_35px_rgba(15,23,42,0.06)] backdrop-blur-sm">
                  <CardContent className="p-7">
                    <div className="mb-5 flex h-12 w-12 items-center justify-center rounded-2xl bg-slate-900 text-white shadow-sm">
                      <Icon className="h-5 w-5" />
                    </div>
                    <h3 className="text-xl font-semibold text-slate-900">{item.title}</h3>
                    <p className="mt-3 text-sm leading-7 text-slate-600">{item.text}</p>
                  </CardContent>
                </Card>
              </motion.div>
            );
          })}
        </div>
      </section>

      <section className="border-y border-slate-200/80 bg-white/70 py-20 backdrop-blur-sm">
        <div className="mx-auto max-w-7xl px-6 sm:px-8 lg:px-10">
          <motion.div
            initial="hidden"
            whileInView="visible"
            viewport={{ once: true, amount: 0.2 }}
            variants={fadeUp}
            transition={{ duration: 0.5 }}
          >
            <SectionTitle
              eyebrow="Tech stack & projects"
              title="Tools I use to turn biological questions into analyzable systems"
              description="I enjoy building practical workflows for research, from genomic analysis pipelines to lightweight lab-facing software tools."
            />
          </motion.div>

          <div className="mt-10 grid gap-6 lg:grid-cols-[1.1fr_0.9fr]">
            <motion.div
              initial="hidden"
              whileInView="visible"
              viewport={{ once: true, amount: 0.2 }}
              variants={fadeUp}
              transition={{ duration: 0.5, delay: 0.05 }}
            >
              <Card className="h-full rounded-[2rem] border-slate-200 bg-gradient-to-br from-slate-950 to-slate-800 text-white shadow-[0_18px_60px_rgba(15,23,42,0.22)]">
                <CardContent className="p-8 sm:p-10">
                  <div className="flex items-center gap-3 text-slate-300">
                    <CodeIcon className="h-5 w-5" />
                    <span className="text-sm uppercase tracking-[0.2em]">Core capabilities</span>
                  </div>

                  <div className="mt-8 space-y-6">
                    <div>
                      <h3 className="text-2xl font-semibold">Computational biology</h3>
                      <p className="mt-2 max-w-2xl text-sm leading-7 text-slate-300">
                        Analyzing genomic data and building lab-specific software tools to support research workflows and interpretation.
                      </p>
                    </div>

                    <div>
                      <h3 className="text-2xl font-semibold">Languages & tools</h3>
                      <p className="mt-2 max-w-2xl text-sm leading-7 text-slate-300">
                        Python, R, Git, and AI coding assistants for rapid prototyping, scripting, and turning ideas into usable analysis pipelines.
                      </p>
                    </div>
                  </div>
                </CardContent>
              </Card>
            </motion.div>

            <div className="grid gap-6">
              {sideCards.map((item, index) => {
                const Icon = item.icon;
                return (
                  <motion.div
                    key={item.title}
                    initial="hidden"
                    whileInView="visible"
                    viewport={{ once: true, amount: 0.2 }}
                    variants={fadeUp}
                    transition={{ duration: 0.45, delay: 0.08 + index * 0.08 }}
                  >
                    <Card className="rounded-[1.75rem] border-slate-200 bg-white shadow-[0_12px_35px_rgba(15,23,42,0.06)]">
                      <CardContent className="p-7">
                        <div className="mb-4 flex h-11 w-11 items-center justify-center rounded-2xl bg-slate-100">
                          <Icon className="h-5 w-5 text-slate-900" />
                        </div>
                        <h3 className="text-xl font-semibold text-slate-900">{item.title}</h3>
                        <p className="mt-3 text-sm leading-7 text-slate-600">{item.text}</p>
                      </CardContent>
                    </Card>
                  </motion.div>
                );
              })}
            </div>
          </div>
        </div>
      </section>

      <section className="mx-auto max-w-7xl px-6 py-20 sm:px-8 lg:px-10">
        <motion.div
          initial="hidden"
          whileInView="visible"
          viewport={{ once: true, amount: 0.2 }}
          variants={fadeUp}
          transition={{ duration: 0.5 }}
          className="grid gap-10 lg:grid-cols-[0.95fr_1.05fr] lg:items-start"
        >
          <SectionTitle
            eyebrow="Beyond the bench"
            title="A little more about me outside the lab"
            description="When I’m not working, I’m usually reading, working out, taking long walks with my dog, or cooking something delicious."
          />

  
          <Card className="overflow-hidden rounded-[2rem] border-0 bg-slate-950 text-white shadow-[0_20px_80px_rgba(15,23,42,0.25)]">
            <CardContent className="relative p-8 sm:p-10 lg:p-12">
              <div className="absolute inset-0 bg-[radial-gradient(circle_at_top_right,rgba(34,211,238,0.18),transparent_28%),radial-gradient(circle_at_bottom_left,rgba(129,140,248,0.16),transparent_30%)]" />
              <div className="relative flex flex-col gap-8 lg:flex-row lg:items-center lg:justify-between">
                <div className="max-w-2xl">
                  <p className="text-sm uppercase tracking-[0.25em] text-slate-400">Connect with me</p>
                  <h2 className="mt-3 text-3xl font-semibold tracking-tight sm:text-4xl">
                    Let’s talk science, computation, and interesting biological questions.
                  </h2>
                  <p className="mt-4 text-base leading-7 text-slate-300">
                    You can use the links below to reach out, browse my work, or adapt this site further with publications, CV links, or project highlights.
                  </p>
                </div>

                <div className="flex flex-wrap gap-4">
                  <Button asChild size="lg" className="rounded-full bg-white text-slate-950 hover:bg-slate-100">
                    <a href={GITHUB_URL} target="_blank" rel="noreferrer">
                      <GitHubIcon className="mr-2 h-4 w-4" />
                      GitHub
                    </a>
                  </Button>
                  <Button asChild size="lg" variant="outline" className="rounded-full border-white/20 bg-transparent text-white hover:bg-white/10 hover:text-white">
                    <a href={`mailto:${EMAIL}`}>
                      <MailIcon className="mr-2 h-4 w-4" />
                      {EMAIL}
                    </a>
                  </Button>
                </div>
              </div>
            </CardContent>
          </Card>
        </motion.div>

        <footer className="mt-8 flex flex-col items-start justify-between gap-3 border-t border-slate-200 pt-6 text-sm text-slate-500 sm:flex-row sm:items-center">
          <p>© {new Date().getFullYear()} Alona Lavi</p>
          <p>Designed for a clean, scientific, and inviting online presence.</p>
        </footer>
      </section>
    </main>
  );
}
