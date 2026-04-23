import { useState, useRef, useEffect, useCallback } from "react";

const C = {
  bg: "#0a0a0f", card: "#13131f", surface: "#1a1a2e", surface2: "#20203a",
  primary: "#ff2d6f", secondary: "#7c3aed", accent: "#00e5ff", gold: "#ffd600",
  text: "#f0f0ff", muted: "#7b7b9a", border: "#2a2a40",
  msgOut: "#ff2d6f", msgIn: "#1e1e35", online: "#00e676", read: "#00e5ff",
};

// Extended SA emoji set — money, animals, places, vibes
const EMOJIS = [
  "❤️","🔥","😂","😍","👏","😮","😢","🎉","👍","💪",
  "🙏","✨","🤌","👀","💯","🇿🇦","🕺","🍲","📸","🌟",
  "💎","🎵","🏆","⚡","🌈","🦁","🐆","🦏","🦒","🐘",
  "🦓","🐊","🦅","🌍","🏔️","🌅","🏙️","🌿","🌻","🌊",
  "💵","💴","💰","🪙","💳","💸","🤑","🏦","💹","🛒",
  "🥳","🎊","🎶","🎤","🎬","🍺","🍗","🥩","🫓","☕",
];

const USERS = [
  { id: 1, name: "Zara Mokoena", handle: "@zaravibes", phone: "+27 82 111 2233", avatar: "ZM", color: "#ff2d6f", followers: "124K", following: "892", posts: 87, verified: true, bio: "Joburg 🔥 Content Creator | Lifestyle & Fashion" },
  { id: 2, name: "Lebo Dlamini", handle: "@lebo.moves", phone: "+27 73 444 5566", avatar: "LD", color: "#7c3aed", followers: "56.2K", following: "441", posts: 203, verified: false, bio: "Dance | Music | Vibes 🎵 East Rand represent" },
  { id: 3, name: "Thabo Khumalo", handle: "@thabocreates", phone: "+27 61 777 8899", avatar: "TK", color: "#00e5ff", followers: "9.8K", following: "312", posts: 45, verified: false, bio: "Photographer 📸 Capturing Mzansi's beauty" },
  { id: 4, name: "Naledi Sithole", handle: "@naledi.s", phone: "+27 79 321 6543", avatar: "NS", color: "#ffd600", followers: "31K", following: "200", posts: 119, verified: true, bio: "Chef 🍲 | Food blogger | Soweto born" },
  { id: 5, name: "Doctor T", handle: "@doctor_t", phone: "+27 74 857 5764", avatar: "DT", color: "#ff6b35", followers: "1.2K", following: "340", posts: 12, verified: false, bio: "Facilities Pro | Content Creator | Daveyton 🇿🇦" },
];
const ME = USERS[4];

const GROUPS = [
  { id: "g1", name: "East Rand Squad 🔥", avatar: "ER", color: "#ff2d6f", members: [USERS[0], USERS[1], USERS[4]], desc: "East Rand vibes only!" },
  { id: "g2", name: "Content Creators ZA 📸", avatar: "CC", color: "#7c3aed", members: [USERS[0], USERS[2], USERS[3], USERS[4]], desc: "SA's finest creators" },
];

const nowTime = () => new Date().toLocaleTimeString([], { hour: "2-digit", minute: "2-digit" });

const INIT_MESSAGES = {
  1: [
    { id: 1, from: 1, text: "Hey! Saw your latest post 😍", time: "10:02", status: "read", reactions: [] },
    { id: 2, from: 5, text: "Thanks! Been working hard on the content 💪", time: "10:04", status: "read", reactions: ["❤️"] },
    { id: 3, from: 1, text: "Yoh that pic was 🔥🔥", time: "10:05", status: "read", reactions: [] },
    { id: 5, from: 5, text: "Working on something big 👀 Stay tuned!", time: "10:08", status: "delivered", reactions: ["👀", "🔥"] },
  ],
  2: [
    { id: 1, from: 2, text: "Bro you need to try my new challenge!", time: "09:30", status: "read", reactions: [] },
    { id: 2, from: 5, text: "Haha I'll give it a shot 😂", time: "09:32", status: "read", reactions: ["😂"] },
    { id: 3, from: 2, text: "Try my new challenge!", time: "09:45", status: "read", reactions: [] },
  ],
  3: [
    { id: 1, from: 3, text: "Check out my latest shots 📸", time: "Yesterday", status: "read", reactions: [] },
    { id: 2, from: 5, text: "Those are amazing bro! Golden hour hit different 🌅", time: "Yesterday", status: "read", reactions: ["😍"] },
  ],
  4: [
    { id: 1, from: 4, text: "Recipe is almost ready 🍲 Will send you a taste test invite!", time: "12m ago", status: "read", reactions: [] },
  ],
  g1: [
    { id: 1, from: 1, text: "Squad meetup this weekend? 🔥", time: "09:00", status: "read", reactions: [], isGroup: true },
    { id: 2, from: 2, text: "I'm in! 🕺", time: "09:05", status: "read", reactions: [], isGroup: true },
    { id: 3, from: 5, text: "Let's do it East Rand stand up! 🇿🇦", time: "09:10", status: "read", reactions: ["❤️", "🔥"], isGroup: true },
  ],
  g2: [
    { id: 1, from: 3, text: "New collab opportunity dropped 👀", time: "08:00", status: "read", reactions: [], isGroup: true },
    { id: 2, from: 4, text: "Send the details!", time: "08:02", status: "read", reactions: [], isGroup: true },
  ],
};

const INIT_CHATS = [
  { id: 1, type: "dm", user: USERS[0], lastMsg: "Working on something big 👀 Stay tuned!", time: "10:08", unread: 0, online: true, pinned: true, muted: false },
  { id: "g1", type: "group", group: GROUPS[0], lastMsg: "Let's do it East Rand stand up! 🇿🇦", time: "09:10", unread: 2, online: false, pinned: true, muted: false },
  { id: 2, type: "dm", user: USERS[1], lastMsg: "Try my new challenge!", time: "09:45", unread: 1, online: true, pinned: false, muted: false },
  { id: "g2", type: "group", group: GROUPS[1], lastMsg: "Send the details!", time: "08:02", unread: 3, online: false, pinned: false, muted: false },
  { id: 3, type: "dm", user: USERS[2], lastMsg: "Those are amazing bro! Golden hour 🌅", time: "Yesterday", unread: 0, online: false, pinned: false, muted: false },
  { id: 4, type: "dm", user: USERS[3], lastMsg: "Recipe is almost ready 🍲", time: "12m ago", unread: 0, online: false, pinned: false, muted: true },
];

const STORIES = [
  { id: 1, user: USERS[0], seen: false },
  { id: 2, user: USERS[1], seen: false },
  { id: 3, user: USERS[2], seen: true },
  { id: 4, user: USERS[3], seen: false },
];

const FEED_POSTS = [
  { id: 1, user: USERS[0], time: "2m ago", content: "Living my best life in Joburg! 🔥✨ The energy here is unmatched. #JoziVibes #Lifestyle", likes: 4821, comments: 312, shares: 98, liked: false, gradient: "linear-gradient(135deg,#ff2d6f,#7c3aed)", emoji: "🌆" },
  { id: 2, user: USERS[3], time: "15m ago", content: "Made pap & chakalaka today 🍲🤌 Recipe dropping tomorrow! #MzansiFood", likes: 2109, comments: 87, shares: 44, liked: true, gradient: "linear-gradient(135deg,#ffd600,#ff6b35)", emoji: "🍲" },
  { id: 3, user: USERS[1], time: "1h ago", content: "New dance challenge is OUT 🕺🔥 Tag me when you try it! #DanceChallenge", likes: 8934, comments: 1204, shares: 567, liked: false, gradient: "linear-gradient(135deg,#7c3aed,#00e5ff)", emoji: "🕺" },
  { id: 4, user: USERS[2], time: "3h ago", content: "Golden hour on the East Rand never disappoints 📸🌅 #Photography #EastRand", likes: 1456, comments: 43, shares: 29, liked: false, gradient: "linear-gradient(135deg,#00e5ff,#1a1a2e)", emoji: "📸" },
];

const REELS = [
  { id: 1, user: USERS[0], likes: "124K", comments: "4.2K", shares: "891", saves: "3.1K", caption: "Day in my life 🎬 Joburg never sleeps! #Joburg #Lifestyle", audio: "🎵 Amapiano Mix - DJ Maphorisa", gradient: "linear-gradient(180deg,#ff2d6f55 0%,#0a0a0f 100%)", bg: "linear-gradient(160deg,#ff2d6f,#7c3aed,#0a0a0f)", emoji: "🎬", tags: ["#Joburg","#Lifestyle","#Mzansi"] },
  { id: 2, user: USERS[1], likes: "89K", comments: "2.1K", shares: "445", saves: "1.8K", caption: "New amapiano dance 🕺 try it! Drop a 🦁 if you got it", audio: "🎵 Kabza De Small - Sponono", gradient: "linear-gradient(180deg,#7c3aed55 0%,#0a0a0f 100%)", bg: "linear-gradient(160deg,#7c3aed,#00e5ff,#0a0a0f)", emoji: "🕺", tags: ["#DanceChallenge","#Amapiano","#EastRand"] },
  { id: 3, user: USERS[3], likes: "45K", comments: "980", shares: "312", saves: "2.4K", caption: "Cooking pap & oxtail stew 🍲 recipe in bio!", audio: "🎵 Ladysmith Black Mambazo - Homeless", gradient: "linear-gradient(180deg,#ffd60055 0%,#0a0a0f 100%)", bg: "linear-gradient(160deg,#ffd600,#ff6b35,#0a0a0f)", emoji: "🍲", tags: ["#MzansiFood","#Cooking","#SouthAfrica"] },
  { id: 4, user: USERS[2], likes: "12K", comments: "310", shares: "88", saves: "560", caption: "Golden hour at Kruger 📸🦁 nothing hits different", audio: "🎵 Freshlyground - Doo Be Doo", gradient: "linear-gradient(180deg,#00e5ff55 0%,#0a0a0f 100%)", bg: "linear-gradient(160deg,#ff8c00,#ffd600,#0a0a0f)", emoji: "🦁", tags: ["#Photography","#Kruger","#Wildlife"] },
];

// Icons
const Ic = ({ n, sz = 22, col = C.muted, active = false }) => {
  const c = active ? C.primary : col;
  const p = { width: sz, height: sz };
  const m = {
    home: <svg {...p} viewBox="0 0 24 24" fill={active?c:"none"} stroke={c} strokeWidth="2"><path d="M3 9l9-7 9 7v11a2 2 0 01-2 2H5a2 2 0 01-2-2z"/><polyline points="9,22 9,12 15,12 15,22"/></svg>,
    reel: <svg {...p} viewBox="0 0 24 24" fill="none" stroke={c} strokeWidth="2"><polygon points="23,7 16,12 23,17"/><rect x="1" y="5" width="15" height="14" rx="2"/></svg>,
    msg:  <svg {...p} viewBox="0 0 24 24" fill={active?c:"none"} stroke={c} strokeWidth="2"><path d="M21 15a2 2 0 01-2 2H7l-4 4V5a2 2 0 012-2h14a2 2 0 012 2z"/></svg>,
    user: <svg {...p} viewBox="0 0 24 24" fill={active?c:"none"} stroke={c} strokeWidth="2"><path d="M20 21v-2a4 4 0 00-4-4H8a4 4 0 00-4 4v2"/><circle cx="12" cy="7" r="4"/></svg>,
    heart:<svg {...p} viewBox="0 0 24 24" fill={active?"#ff2d6f":"none"} stroke={active?"#ff2d6f":c} strokeWidth="2"><path d="M20.84 4.61a5.5 5.5 0 00-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 00-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 000-7.78z"/></svg>,
    cmnt: <svg {...p} viewBox="0 0 24 24" fill="none" stroke={c} strokeWidth="2"><path d="M21 15a2 2 0 01-2 2H7l-4 4V5a2 2 0 012-2h14a2 2 0 012 2z"/></svg>,
    shr:  <svg {...p} viewBox="0 0 24 24" fill="none" stroke={c} strokeWidth="2"><circle cx="18" cy="5" r="3"/><circle cx="6" cy="12" r="3"/><circle cx="18" cy="19" r="3"/><line x1="8.59" y1="13.51" x2="15.42" y2="17.49"/><line x1="15.41" y1="6.51" x2="8.59" y2="10.49"/></svg>,
    back: <svg {...p} viewBox="0 0 24 24" fill="none" stroke={c} strokeWidth="2.5"><polyline points="15,18 9,12 15,6"/></svg>,
    send: <svg {...p} viewBox="0 0 24 24" fill="none" stroke={c} strokeWidth="2"><line x1="22" y1="2" x2="11" y2="13"/><polygon points="22,2 15,22 11,13 2,9"/></svg>,
    mic:  <svg {...p} viewBox="0 0 24 24" fill="none" stroke={c} strokeWidth="2"><rect x="9" y="2" width="6" height="11" rx="3"/><path d="M19 10v2a7 7 0 01-14 0v-2"/><line x1="12" y1="19" x2="12" y2="23"/><line x1="8" y1="23" x2="16" y2="23"/></svg>,
    emo:  <svg {...p} viewBox="0 0 24 24" fill="none" stroke={c} strokeWidth="2"><circle cx="12" cy="12" r="10"/><path d="M8 14s1.5 2 4 2 4-2 4-2"/><line x1="9" y1="9" x2="9.01" y2="9"/><line x1="15" y1="9" x2="15.01" y2="9"/></svg>,
    att:  <svg {...p} viewBox="0 0 24 24" fill="none" stroke={c} strokeWidth="2"><path d="M21.44 11.05l-9.19 9.19a6 6 0 01-8.49-8.49l9.19-9.19a4 4 0 015.66 5.66l-9.2 9.19a2 2 0 01-2.83-2.83l8.49-8.48"/></svg>,
    cam:  <svg {...p} viewBox="0 0 24 24" fill="none" stroke={c} strokeWidth="2"><path d="M23 19a2 2 0 01-2 2H3a2 2 0 01-2-2V8a2 2 0 012-2h4l2-3h6l2 3h4a2 2 0 012 2z"/><circle cx="12" cy="13" r="4"/></svg>,
    srch: <svg {...p} viewBox="0 0 24 24" fill="none" stroke={c} strokeWidth="2"><circle cx="11" cy="11" r="8"/><line x1="21" y1="21" x2="16.65" y2="16.65"/></svg>,
    mute: <svg {...p} viewBox="0 0 24 24" fill="none" stroke={c} strokeWidth="2"><path d="M9 9v3a3 3 0 006 0V9"/><path d="M17 16.95A7 7 0 015 12v-2"/><path d="M19 19L5 5"/><line x1="1" y1="1" x2="23" y2="23"/></svg>,
    t2:   <svg {...p} viewBox="0 0 24 24" fill="none" stroke={c} strokeWidth="2.5"><polyline points="1,12 5,16 11,6"/><polyline points="9,12 13,16 19,6"/></svg>,
    t1:   <svg {...p} viewBox="0 0 24 24" fill="none" stroke={c} strokeWidth="2.5"><polyline points="5,12 9,16 19,6"/></svg>,
    vfy:  <svg width={15} height={15} viewBox="0 0 24 24" fill={C.accent}><path d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/></svg>,
    more: <svg {...p} viewBox="0 0 24 24" fill={c}><circle cx="5" cy="12" r="2"/><circle cx="12" cy="12" r="2"/><circle cx="19" cy="12" r="2"/></svg>,
    x:    <svg {...p} viewBox="0 0 24 24" fill="none" stroke={c} strokeWidth="2"><line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/></svg>,
    ph:   <svg {...p} viewBox="0 0 24 24" fill="none" stroke={c} strokeWidth="2"><path d="M22 16.92v3a2 2 0 01-2.18 2 19.79 19.79 0 01-8.63-3.07A19.5 19.5 0 013.07 10.8 19.79 19.79 0 01.01 2.18 2 2 0 012 .01h3a2 2 0 012 1.72 12.84 12.84 0 00.7 2.81 2 2 0 01-.45 2.11L6.09 7.91a16 16 0 006 6l1.27-1.27a2 2 0 012.11-.45 12.84 12.84 0 002.81.7A2 2 0 0122 14.92z"/></svg>,
    vid2: <svg {...p} viewBox="0 0 24 24" fill="none" stroke={c} strokeWidth="2"><polygon points="23,7 16,12 23,17"/><rect x="1" y="5" width="15" height="14" rx="2"/></svg>,
    grp:  <svg {...p} viewBox="0 0 24 24" fill="none" stroke={c} strokeWidth="2"><path d="M17 21v-2a4 4 0 00-4-4H5a4 4 0 00-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 00-3-3.87"/><path d="M16 3.13a4 4 0 010 7.75"/></svg>,
    save: <svg {...p} viewBox="0 0 24 24" fill={active?"#ffd600":"none"} stroke={active?"#ffd600":c} strokeWidth="2"><polygon points="19,21 12,16 5,21 5,3 19,3"/></svg>,
    phone2:<svg {...p} viewBox="0 0 24 24" fill="none" stroke={c} strokeWidth="2"><path d="M22 16.92v3a2 2 0 01-2.18 2 19.79 19.79 0 01-8.63-3.07A19.5 19.5 0 013.07 10.8"/><path d="M1 1l22 22"/></svg>,
    adduser:<svg {...p} viewBox="0 0 24 24" fill="none" stroke={c} strokeWidth="2"><path d="M16 21v-2a4 4 0 00-4-4H5a4 4 0 00-4 4v2"/><circle cx="8.5" cy="7" r="4"/><line x1="20" y1="8" x2="20" y2="14"/><line x1="23" y1="11" x2="17" y2="11"/></svg>,
  };
  return m[n] || null;
};

const Av = ({ user, group, size = 40, border = false, online = false }) => {
  const d = group || user;
  return (
    <div style={{ position:"relative", flexShrink:0 }}>
      <div style={{ width:size, height:size, borderRadius:"50%", background:border?`linear-gradient(135deg,${C.primary},${C.secondary},${C.accent})`:"transparent", padding:border?2:0, display:"flex", alignItems:"center", justifyContent:"center" }}>
        <div style={{ width:border?size-4:size, height:border?size-4:size, borderRadius:"50%", background:d.color, display:"flex", alignItems:"center", justifyContent:"center", fontSize:size*0.33, fontWeight:800, color:"#fff", border:border?`2px solid ${C.bg}`:"none", fontFamily:"'Bebas Neue',sans-serif", letterSpacing:1 }}>
          {d.avatar}
        </div>
      </div>
      {online && <div style={{ position:"absolute", bottom:1, right:1, width:size*0.27, height:size*0.27, borderRadius:"50%", background:C.online, border:`2px solid ${C.bg}` }} />}
    </div>
  );
};

const fN = n => typeof n==="number"?(n>=1000?`${(n/1000).toFixed(1)}K`:n):n;

const Receipt = ({ s }) => {
  if(s==="sending") return <span style={{color:C.muted,fontSize:10}}>⏳</span>;
  if(s==="sent")     return <Ic n="t1" sz={13} col={C.muted}/>;
  if(s==="delivered")return <Ic n="t2" sz={13} col={C.muted}/>;
  if(s==="read")     return <Ic n="t2" sz={13} col={C.read}/>;
  return null;
};

const TypingDots = () => (
  <div style={{ display:"flex", gap:4, alignItems:"center", padding:"9px 14px", background:C.msgIn, borderRadius:"18px 18px 18px 4px", width:"fit-content" }}>
    <style>{`@keyframes bd{0%,80%,100%{transform:translateY(0)}40%{transform:translateY(-5px)}}`}</style>
    {[0,.2,.4].map((d,i)=><div key={i} style={{ width:7,height:7,borderRadius:"50%",background:C.muted,animation:`bd 1.2s ease-in-out ${d}s infinite` }}/>)}
  </div>
);

function ChatRow({ chat, onOpen }) {
  const isG = chat.type==="group";
  const name = isG ? chat.group.name : chat.user.name;
  return (
    <div onClick={()=>onOpen(chat)} style={{ padding:"12px 18px", display:"flex", alignItems:"center", gap:13, cursor:"pointer", borderBottom:`1px solid ${C.border}20` }}
      onMouseEnter={e=>e.currentTarget.style.background=C.surface+"50"}
      onMouseLeave={e=>e.currentTarget.style.background="transparent"}>
      <div style={{position:"relative"}}>
        {isG?<Av group={chat.group} size={52}/>:<Av user={chat.user} size={52} online={chat.online}/>}
        {chat.pinned&&<div style={{position:"absolute",bottom:-2,right:-2,background:C.gold,borderRadius:"50%",width:16,height:16,display:"flex",alignItems:"center",justifyContent:"center",fontSize:8,border:`2px solid ${C.bg}`}}>📌</div>}
      </div>
      <div style={{flex:1,minWidth:0}}>
        <div style={{display:"flex",justifyContent:"space-between",marginBottom:3}}>
          <div style={{display:"flex",alignItems:"center",gap:5}}>
            <span style={{color:chat.unread>0?C.text:C.muted,fontWeight:chat.unread>0?700:500,fontSize:15}}>{name}</span>
            {isG&&<span style={{fontSize:10}}>👥</span>}
            {chat.muted&&<Ic n="mute" sz={13} col={C.muted}/>}
          </div>
          <span style={{color:chat.unread>0?C.primary:C.muted,fontSize:11,fontWeight:chat.unread>0?700:400,flexShrink:0}}>{chat.time}</span>
        </div>
        <div style={{display:"flex",alignItems:"center",justifyContent:"space-between"}}>
          <span style={{color:C.muted,fontSize:13,overflow:"hidden",textOverflow:"ellipsis",whiteSpace:"nowrap",flex:1}}>{chat.lastMsg}</span>
          {chat.unread>0&&<div style={{background:chat.muted?C.muted:C.primary,borderRadius:10,minWidth:20,height:20,display:"flex",alignItems:"center",justifyContent:"center",fontSize:10,fontWeight:800,color:"#fff",marginLeft:8,padding:"0 5px"}}>{chat.unread}</div>}
        </div>
      </div>
    </div>
  );
}

export default function App() {
  // Messages is the default (first) tab
  const [tab, setTab]         = useState("messages");
  const [posts, setPosts]     = useState(FEED_POSTS);
  const [chats, setChats]     = useState(INIT_CHATS);
  const [msgs, setMsgs]       = useState(INIT_MESSAGES);
  const [openChat, setOpenChat] = useState(null);
  const [input, setInput]     = useState("");
  const [typing, setTyping]   = useState({});
  const [showEmo, setShowEmo] = useState(false);
  const [replyTo, setReplyTo] = useState(null);
  const [lpMsg, setLpMsg]     = useState(null);
  const [recording, setRec]   = useState(false);
  const [recSecs, setRecSecs] = useState(0);
  const [search, setSearch]   = useState("");
  const [chatTab, setChatTab] = useState("all");
  const [openStory, setOpenStory] = useState(null);
  const [storyPct, setStoryPct]   = useState(0);
  const [viewProf, setViewProf]   = useState(null);
  const [followed, setFollowed]   = useState({1:true,2:false,3:false,4:true});
  const [activeReel, setActiveReel] = useState(0);
  const [reelLiked, setReelLiked] = useState({});
  const [reelSaved, setReelSaved] = useState({});
  const [showAddPhone, setShowAddPhone] = useState(false);
  const [phoneInput, setPhoneInput] = useState("");
  const [phoneResult, setPhoneResult] = useState(null);
  const [phoneSearched, setPhoneSearched] = useState(false);

  const endRef    = useRef(null);
  const inRef     = useRef(null);
  const recTimer  = useRef(null);
  const stTimer   = useRef(null);
  const lpTimer   = useRef(null);

  useEffect(()=>{ endRef.current?.scrollIntoView({behavior:"smooth"}); },[msgs,openChat,typing]);

  useEffect(()=>{
    if(openStory!==null){
      setStoryPct(0);
      stTimer.current=setInterval(()=>setStoryPct(p=>{ if(p>=100){clearInterval(stTimer.current);setOpenStory(null);return 0;}return p+2; }),60);
    }
    return ()=>clearInterval(stTimer.current);
  },[openStory]);

  useEffect(()=>{
    if(recording){ recTimer.current=setInterval(()=>setRecSecs(s=>s+1),1000); }
    else{ clearInterval(recTimer.current); setRecSecs(0); }
    return ()=>clearInterval(recTimer.current);
  },[recording]);

  const getUser = id=>USERS.find(u=>u.id===id);

  const simulateReply = useCallback((chatId, chat)=>{
    const sender = chat.type==="dm" ? chat.user : chat.group.members.find(m=>m.id!==ME.id);
    const replies=["That's so true! 🔥","Haha yoh! 😂","Facts bro 💯","Eish you right 😅","For real for real 🙌","No ways! 😮","Say less 👌","Sharp sharp! 🇿🇦","Lol I can't 😂🔥","That's the one! ✨","Ayy let's go! 🎉","Wena! 😂🔥","Sho't left! 🦁","Yebo! 💯"];
    setTimeout(()=>{
      setTyping(t=>({...t,[chatId]:true}));
      setTimeout(()=>{
        setTyping(t=>({...t,[chatId]:false}));
        const nm={id:Date.now(),from:sender.id,text:replies[Math.floor(Math.random()*replies.length)],time:nowTime(),status:"read",reactions:[],isGroup:chat.type==="group"};
        setMsgs(m=>({...m,[chatId]:[...(m[chatId]||[]),nm]}));
        setChats(prev=>prev.map(c=>c.id===chatId?{...c,lastMsg:nm.text,time:nowTime()}:c));
      },1800+Math.random()*1000);
    },600+Math.random()*700);
  },[]);

  const send = (chatId, chat)=>{
    if(!input.trim()) return;
    const nm={id:Date.now(),from:5,text:input.trim(),time:nowTime(),status:"sending",reactions:[],replyTo:replyTo?{text:replyTo.text,from:replyTo.from}:null};
    setMsgs(m=>({...m,[chatId]:[...(m[chatId]||[]),nm]}));
    setChats(prev=>prev.map(c=>c.id===chatId?{...c,lastMsg:nm.text,time:nowTime(),unread:0}:c));
    setInput(""); setReplyTo(null); setShowEmo(false);
    const upd=(id,st,delay)=>setTimeout(()=>setMsgs(m=>({...m,[chatId]:m[chatId].map(x=>x.id===id?{...x,status:st}:x)})),delay);
    upd(nm.id,"sent",500); upd(nm.id,"delivered",1200); upd(nm.id,"read",2500);
    simulateReply(chatId, chat);
  };

  const sendVoice=(chatId,chat)=>{
    if(recSecs<1){setRec(false);return;}
    const dur=recSecs; setRec(false);
    const nm={id:Date.now(),from:5,text:"",time:nowTime(),status:"sending",reactions:[],voiceNote:{duration:dur}};
    setMsgs(m=>({...m,[chatId]:[...(m[chatId]||[]),nm]}));
    setChats(prev=>prev.map(c=>c.id===chatId?{...c,lastMsg:`🎙️ Voice note (${dur}s)`,time:nowTime()}:c));
    setTimeout(()=>setMsgs(m=>({...m,[chatId]:m[chatId].map(x=>x.id===nm.id?{...x,status:"read"}:x)})),2000);
    simulateReply(chatId,chat);
  };

  const react=(chatId,msgId,emoji)=>{
    setMsgs(m=>({...m,[chatId]:m[chatId].map(x=>x.id!==msgId?x:{...x,reactions:x.reactions.includes(emoji)?x.reactions.filter(r=>r!==emoji):[...x.reactions,emoji]})}));
    setLpMsg(null);
  };

  const openChatFn=(chat)=>{ setOpenChat(chat); setChats(p=>p.map(c=>c.id===chat.id?{...c,unread:0}:c)); };

  const searchByPhone = () => {
    const cleaned = phoneInput.replace(/\s/g,"");
    const found = USERS.find(u=>u.phone&&u.phone.replace(/\s/g,"")===cleaned && u.id!==ME.id);
    setPhoneResult(found||null);
    setPhoneSearched(true);
  };

  const filtered=chats.filter(c=>{
    const n=c.type==="dm"?c.user.name:c.group.name;
    const m=(n+c.lastMsg).toLowerCase().includes(search.toLowerCase());
    if(!m)return false;
    if(chatTab==="groups") return c.type==="group";
    if(chatTab==="unread") return c.unread>0;
    return true;
  });

  const totalUnread=chats.reduce((s,c)=>s+c.unread,0);

  // Story viewer
  if(openStory!==null){
    const s=STORIES[openStory];
    return(
      <div style={{width:"100%",maxWidth:430,margin:"0 auto",height:"100vh",background:s.user.color,display:"flex",flexDirection:"column",fontFamily:"'DM Sans',sans-serif",position:"relative",overflow:"hidden"}}>
        <div style={{position:"absolute",top:0,left:0,right:0,padding:"14px 16px 0",zIndex:10}}>
          <div style={{display:"flex",gap:4,marginBottom:12}}>
            {STORIES.map((_,i)=>(
              <div key={i} style={{flex:1,height:3,borderRadius:2,background:i<openStory?"#fff":"rgba(255,255,255,0.3)",position:"relative",overflow:"hidden"}}>
                {i===openStory&&<div style={{position:"absolute",left:0,top:0,bottom:0,width:`${storyPct}%`,background:"#fff",transition:"width 0.06s linear"}}/>}
              </div>
            ))}
          </div>
          <div style={{display:"flex",alignItems:"center",gap:10}}>
            <Av user={s.user} size={38}/>
            <div><div style={{color:"#fff",fontWeight:700,fontSize:14}}>{s.user.name}</div><div style={{color:"rgba(255,255,255,0.7)",fontSize:11}}>Just now</div></div>
            <button onClick={()=>setOpenStory(null)} style={{marginLeft:"auto",background:"none",border:"none",color:"#fff",fontSize:22,cursor:"pointer"}}>✕</button>
          </div>
        </div>
        <div style={{flex:1,display:"flex",alignItems:"center",justifyContent:"center",flexDirection:"column",gap:12}}>
          <div style={{fontSize:80}}>✨</div>
          <div style={{color:"#fff",fontSize:20,fontWeight:800,fontFamily:"'Bebas Neue',sans-serif",letterSpacing:2}}>{s.user.name}'s Story</div>
          <div style={{color:"rgba(255,255,255,0.8)",fontSize:14}}>Living life to the fullest 🔥</div>
        </div>
        <div style={{padding:"0 20px 40px",display:"flex",gap:10}}>
          <input placeholder="Reply to story..." style={{flex:1,background:"rgba(255,255,255,0.15)",border:"1px solid rgba(255,255,255,0.3)",borderRadius:24,padding:"11px 16px",color:"#fff",fontSize:14,outline:"none"}}/>
          <button onClick={()=>setOpenStory(openStory<STORIES.length-1?openStory+1:null)} style={{background:"#fff",border:"none",borderRadius:"50%",width:44,height:44,fontSize:18,cursor:"pointer"}}>→</button>
        </div>
      </div>
    );
  }

  // Profile view
  if(viewProf!==null){
    const u=USERS.find(x=>x.id===viewProf);
    return(
      <div style={{width:"100%",maxWidth:430,margin:"0 auto",height:"100vh",background:C.bg,display:"flex",flexDirection:"column",fontFamily:"'DM Sans',sans-serif",overflow:"hidden"}}>
        <div style={{padding:"16px 20px 0",display:"flex",alignItems:"center",gap:10}}>
          <button onClick={()=>setViewProf(null)} style={{background:"none",border:"none",cursor:"pointer"}}><Ic n="back" col={C.text} sz={24}/></button>
          <span style={{color:C.text,fontSize:18,fontWeight:700,fontFamily:"'Bebas Neue',sans-serif",letterSpacing:1}}>{u.handle}</span>
          {u.verified&&<Ic n="vfy"/>}
        </div>
        <div style={{flex:1,overflowY:"auto"}}>
          <div style={{background:`linear-gradient(180deg,${u.color}44 0%,transparent 100%)`,padding:"28px 20px 20px",textAlign:"center"}}>
            <Av user={u} size={88} border/>
            <div style={{marginTop:14,color:C.text,fontWeight:800,fontSize:22,fontFamily:"'Bebas Neue',sans-serif",letterSpacing:1.5,display:"flex",alignItems:"center",justifyContent:"center",gap:6}}>{u.name} {u.verified&&<Ic n="vfy"/>}</div>
            <div style={{color:C.muted,fontSize:13,marginBottom:6}}>{u.handle}</div>
            <div style={{color:C.text,fontSize:14,marginBottom:18}}>{u.bio}</div>
            <div style={{display:"flex",justifyContent:"center",gap:28,marginBottom:20}}>
              {[["Posts",u.posts],["Followers",u.followers],["Following",u.following]].map(([l,v])=>(
                <div key={l}><div style={{color:C.text,fontWeight:800,fontSize:18,fontFamily:"'Bebas Neue',sans-serif"}}>{v}</div><div style={{color:C.muted,fontSize:12}}>{l}</div></div>
              ))}
            </div>
            {u.id!==ME.id&&(
              <div style={{display:"flex",gap:10,justifyContent:"center"}}>
                <button onClick={()=>setFollowed(f=>({...f,[u.id]:!f[u.id]}))} style={{background:followed[u.id]?C.surface:`linear-gradient(135deg,${C.primary},${C.secondary})`,border:followed[u.id]?`1px solid ${C.border}`:"none",borderRadius:12,padding:"10px 24px",color:C.text,fontWeight:700,cursor:"pointer",fontSize:14}}>
                  {followed[u.id]?"Following ✓":"Follow"}
                </button>
                <button onClick={()=>{setViewProf(null);setTab("messages");const ch=chats.find(c=>c.type==="dm"&&c.user?.id===u.id);if(ch)openChatFn(ch);}} style={{background:C.surface,border:`1px solid ${C.border}`,borderRadius:12,padding:"10px 20px",color:C.text,fontWeight:700,cursor:"pointer",fontSize:14}}>
                  Message
                </button>
              </div>
            )}
          </div>
          <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr",gap:2,padding:"0 2px"}}>
            {Array.from({length:Math.min(u.posts,9)},(_,i)=>(
              <div key={i} style={{aspectRatio:"1",background:`hsl(${(i*37+u.id*70)%360},60%,25%)`,borderRadius:4,display:"flex",alignItems:"center",justifyContent:"center",fontSize:30,cursor:"pointer"}}>
                {["🌅","🎵","🍲","📸","🔥","✨","🦁","🎬","🏆"][i%9]}
              </div>
            ))}
          </div>
        </div>
      </div>
    );
  }

  // Chat screen
  if(openChat&&tab==="messages"){
    const cid=openChat.id;
    const cMsgs=msgs[cid]||[];
    const isG=openChat.type==="group";
    const chatName=isG?openChat.group.name:openChat.user.name;
    const isOn=!isG&&openChat.online;
    const members=isG?openChat.group.members:null;
    const isTyp=typing[cid];

    return(
      <div style={{width:"100%",maxWidth:430,margin:"0 auto",height:"100vh",background:C.bg,display:"flex",flexDirection:"column",fontFamily:"'DM Sans',sans-serif",position:"relative"}}
        onClick={()=>{setLpMsg(null);if(showEmo)setShowEmo(false);}}>

        <div style={{padding:"12px 14px",display:"flex",alignItems:"center",gap:10,background:C.card,borderBottom:`1px solid ${C.border}`,flexShrink:0}}>
          <button onClick={()=>{setOpenChat(null);setReplyTo(null);setShowEmo(false);}} style={{background:"none",border:"none",cursor:"pointer",padding:4}}><Ic n="back" col={C.text} sz={24}/></button>
          <div onClick={()=>!isG&&setViewProf(openChat.user.id)} style={{cursor:"pointer"}}>
            {isG?<Av group={openChat.group} size={42}/>:<Av user={openChat.user} size={42} online={isOn}/>}
          </div>
          <div style={{flex:1,minWidth:0}}>
            <div style={{color:C.text,fontWeight:700,fontSize:15,display:"flex",alignItems:"center",gap:5}}>
              {chatName} {!isG&&openChat.user.verified&&<Ic n="vfy"/>}
              {isG&&<span style={{fontSize:11,color:C.muted,fontWeight:400}}>({members.length})</span>}
            </div>
            <div style={{color:isTyp?C.accent:isOn?C.online:C.muted,fontSize:12}}>
              {isTyp?"typing...":isG?members.map(m=>m.name.split(" ")[0]).join(", "):isOn?"Online":"Last seen recently"}
            </div>
          </div>
          <button style={{background:"none",border:"none",cursor:"pointer",padding:6}}><Ic n="ph" col={C.muted} sz={20}/></button>
          <button style={{background:"none",border:"none",cursor:"pointer",padding:6}}><Ic n="vid2" col={C.muted} sz={20}/></button>
        </div>

        <div style={{flex:1,overflowY:"auto",padding:"12px 12px",display:"flex",flexDirection:"column",gap:3}}>
          <div style={{textAlign:"center",marginBottom:8}}>
            <span style={{background:C.surface,color:C.muted,fontSize:11,padding:"4px 12px",borderRadius:20}}>Today</span>
          </div>
          {cMsgs.map((msg,idx)=>{
            const isMe=msg.from===5;
            const sender=getUser(msg.from);
            const prevFrom=idx>0?cMsgs[idx-1].from:null;
            const showAv=isG&&!isMe&&prevFrom!==msg.from;
            const showName=isG&&!isMe&&showAv;
            return(
              <div key={msg.id}>
                {showName&&<div style={{color:sender?.color||C.muted,fontSize:11,fontWeight:700,marginLeft:44,marginBottom:2,marginTop:6}}>{sender?.name}</div>}
                <div style={{display:"flex",justifyContent:isMe?"flex-end":"flex-start",alignItems:"flex-end",gap:6}}>
                  {isG&&!isMe&&(
                    <div style={{width:34,flexShrink:0,marginBottom:4}}>
                      {showAv&&<Av user={sender} size={30}/>}
                    </div>
                  )}
                  <div
                    onMouseDown={()=>{ lpTimer.current=setTimeout(()=>setLpMsg(msg.id),500); }}
                    onMouseUp={()=>clearTimeout(lpTimer.current)}
                    onTouchStart={()=>{ lpTimer.current=setTimeout(()=>setLpMsg(msg.id),500); }}
                    onTouchEnd={()=>clearTimeout(lpTimer.current)}
                    onClick={e=>{e.stopPropagation();}}
                    style={{maxWidth:"76%",cursor:"pointer",position:"relative"}}>
                    {msg.replyTo&&(
                      <div style={{background:isMe?"rgba(0,0,0,0.25)":C.surface2,borderLeft:`3px solid ${C.accent}`,borderRadius:"8px 8px 0 0",padding:"6px 10px",marginBottom:-4,maxWidth:"100%"}}>
                        <div style={{color:C.accent,fontSize:11,fontWeight:700}}>{getUser(msg.replyTo.from)?.name||"You"}</div>
                        <div style={{color:C.muted,fontSize:12,overflow:"hidden",textOverflow:"ellipsis",whiteSpace:"nowrap"}}>{msg.replyTo.text}</div>
                      </div>
                    )}
                    <div style={{background:isMe?`linear-gradient(135deg,${C.primary},${C.secondary})`:C.msgIn,borderRadius:msg.replyTo?(isMe?"0 0 4px 18px":"0 0 18px 4px"):(isMe?"18px 18px 4px 18px":"18px 18px 18px 4px"),padding:msg.voiceNote?"10px 14px":"10px 13px",boxShadow:isMe?`0 4px 14px ${C.primary}40`:"none",minWidth:80}}>
                      {msg.voiceNote?(
                        <div style={{display:"flex",alignItems:"center",gap:10,minWidth:160}}>
                          <div style={{width:34,height:34,borderRadius:"50%",background:"rgba(255,255,255,0.2)",display:"flex",alignItems:"center",justifyContent:"center",fontSize:14,cursor:"pointer"}}>▶</div>
                          <div style={{flex:1}}>
                            <div style={{display:"flex",alignItems:"center",gap:2,marginBottom:4}}>
                              {Array.from({length:20},(_,i)=>(
                                <div key={i} style={{width:3,borderRadius:2,background:"rgba(255,255,255,0.5)",height:`${8+Math.abs(Math.sin(i*0.8))*16}px`}}/>
                              ))}
                            </div>
                            <div style={{color:"rgba(255,255,255,0.6)",fontSize:11}}>🎙️ {msg.voiceNote.duration}s</div>
                          </div>
                        </div>
                      ):(
                        <div style={{color:C.text,fontSize:14,lineHeight:1.45,wordBreak:"break-word"}}>{msg.text}</div>
                      )}
                      <div style={{display:"flex",alignItems:"center",justifyContent:"flex-end",gap:4,marginTop:4}}>
                        <span style={{color:"rgba(255,255,255,0.45)",fontSize:10}}>{msg.time}</span>
                        {isMe&&<Receipt s={msg.status}/>}
                      </div>
                    </div>
                    {msg.reactions.length>0&&(
                      <div style={{display:"flex",flexWrap:"wrap",gap:3,marginTop:4,justifyContent:isMe?"flex-end":"flex-start"}}>
                        {[...new Set(msg.reactions)].map(r=>(
                          <div key={r} onClick={()=>react(cid,msg.id,r)} style={{background:C.surface2,borderRadius:10,padding:"2px 6px",fontSize:12,cursor:"pointer",border:`1px solid ${C.border}`}}>
                            {r}<span style={{fontSize:10,color:C.muted,marginLeft:2}}>{msg.reactions.filter(x=>x===r).length}</span>
                          </div>
                        ))}
                      </div>
                    )}
                    {lpMsg===msg.id&&(
                      <div onClick={e=>e.stopPropagation()} style={{position:"absolute",[isMe?"right":"left"]:0,bottom:"calc(100% + 8px)",background:C.card,borderRadius:16,padding:12,zIndex:200,boxShadow:"0 8px 32px rgba(0,0,0,0.7)",border:`1px solid ${C.border}`,minWidth:220}}>
                        <div style={{display:"flex",gap:4,marginBottom:10,paddingBottom:10,borderBottom:`1px solid ${C.border}`,flexWrap:"wrap"}}>
                          {EMOJIS.slice(0,12).map(e=>(
                            <button key={e} onClick={()=>react(cid,msg.id,e)} style={{background:msg.reactions.includes(e)?C.surface2:"none",border:msg.reactions.includes(e)?`1px solid ${C.primary}`:"none",borderRadius:8,fontSize:20,cursor:"pointer",padding:3}}>{e}</button>
                          ))}
                        </div>
                        {[["↩️  Reply",()=>{setReplyTo(msg);setLpMsg(null);setTimeout(()=>inRef.current?.focus(),100);}],
                          ["📋  Copy",()=>{navigator.clipboard?.writeText(msg.text||"");setLpMsg(null);}],
                          ["⭐  Star message",()=>setLpMsg(null)],
                          ["🗑️  Delete",()=>{setMsgs(m=>({...m,[cid]:m[cid].filter(x=>x.id!==msg.id)}));setLpMsg(null);}]
                        ].map(([label,fn])=>(
                          <button key={label} onClick={fn} style={{display:"block",width:"100%",background:"none",border:"none",color:label.includes("Delete")?C.primary:C.text,fontSize:14,padding:"9px 8px",textAlign:"left",cursor:"pointer",borderRadius:8,fontFamily:"'DM Sans',sans-serif"}}>{label}</button>
                        ))}
                      </div>
                    )}
                  </div>
                </div>
              </div>
            );
          })}
          {isTyp&&(
            <div style={{display:"flex",alignItems:"flex-end",gap:6,marginTop:4}}>
              {isG&&<div style={{width:34}}/>}
              <TypingDots/>
            </div>
          )}
          <div ref={endRef}/>
        </div>

        {replyTo&&(
          <div style={{padding:"8px 14px",background:C.surface,borderTop:`1px solid ${C.border}`,display:"flex",alignItems:"center",gap:10,flexShrink:0}}>
            <div style={{flex:1,borderLeft:`3px solid ${C.accent}`,paddingLeft:10}}>
              <div style={{color:C.accent,fontSize:11,fontWeight:700}}>Replying to {getUser(replyTo.from)?.name||"yourself"}</div>
              <div style={{color:C.muted,fontSize:13,overflow:"hidden",textOverflow:"ellipsis",whiteSpace:"nowrap"}}>{replyTo.text}</div>
            </div>
            <button onClick={()=>setReplyTo(null)} style={{background:"none",border:"none",cursor:"pointer"}}><Ic n="x" col={C.muted} sz={18}/></button>
          </div>
        )}

        {showEmo&&(
          <div onClick={e=>e.stopPropagation()} style={{background:C.card,borderTop:`1px solid ${C.border}`,padding:"10px 12px",display:"flex",flexWrap:"wrap",gap:6,flexShrink:0,maxHeight:160,overflowY:"auto"}}>
            {EMOJIS.map(e=>(
              <button key={e} onClick={()=>setInput(i=>i+e)} style={{background:"none",border:"none",fontSize:22,cursor:"pointer",padding:2}}>{e}</button>
            ))}
          </div>
        )}

        {recording?(
          <div style={{padding:"12px 14px",background:C.card,borderTop:`1px solid ${C.border}`,display:"flex",alignItems:"center",gap:12,flexShrink:0}}>
            <style>{`@keyframes pulse{0%,100%{opacity:1}50%{opacity:.3}}`}</style>
            <div style={{width:12,height:12,borderRadius:"50%",background:C.primary,animation:"pulse 1s infinite"}}/>
            <div style={{flex:1}}>
              <div style={{color:C.primary,fontWeight:700,fontSize:14}}>Recording... {recSecs}s</div>
              <div style={{height:4,background:C.border,borderRadius:2,marginTop:5}}>
                <div style={{width:`${Math.min(recSecs*3,100)}%`,height:"100%",background:`linear-gradient(90deg,${C.primary},${C.secondary})`,borderRadius:2,transition:"width 1s linear"}}/>
              </div>
            </div>
            <button onClick={()=>setRec(false)} style={{background:C.surface,border:`1px solid ${C.border}`,borderRadius:10,padding:"8px 12px",color:C.muted,cursor:"pointer",fontSize:13}}>✕</button>
            <button onClick={()=>sendVoice(cid,openChat)} style={{background:`linear-gradient(135deg,${C.primary},${C.secondary})`,border:"none",borderRadius:"50%",width:44,height:44,display:"flex",alignItems:"center",justifyContent:"center",cursor:"pointer",boxShadow:`0 4px 14px ${C.primary}50`}}>
              <Ic n="send" col="#fff" sz={18}/>
            </button>
          </div>
        ):(
          <div style={{padding:"8px 10px",background:C.card,borderTop:`1px solid ${C.border}`,display:"flex",alignItems:"flex-end",gap:6,flexShrink:0}}>
            <button onClick={()=>setShowEmo(s=>!s)} style={{background:"none",border:"none",cursor:"pointer",padding:6,flexShrink:0,marginBottom:2}}>
              <Ic n="emo" col={showEmo?C.accent:C.muted} sz={22}/>
            </button>
            <div style={{flex:1,background:C.surface,borderRadius:22,padding:"8px 12px",display:"flex",alignItems:"flex-end",gap:6}}>
              <textarea
                ref={inRef}
                value={input}
                onChange={e=>setInput(e.target.value)}
                onKeyDown={e=>{if(e.key==="Enter"&&!e.shiftKey){e.preventDefault();send(cid,openChat);}}}
                placeholder="Message..."
                rows={1}
                style={{flex:1,background:"none",border:"none",color:C.text,fontSize:14,outline:"none",resize:"none",fontFamily:"'DM Sans',sans-serif",lineHeight:1.4,maxHeight:100,overflowY:"auto"}}
              />
              <button style={{background:"none",border:"none",cursor:"pointer",padding:"0 0 0 4px",flexShrink:0}}><Ic n="att" col={C.muted} sz={19}/></button>
              <button style={{background:"none",border:"none",cursor:"pointer",padding:"0 0 0 4px",flexShrink:0}}><Ic n="cam" col={C.muted} sz={19}/></button>
            </div>
            {input.trim()?(
              <button onClick={()=>send(cid,openChat)} style={{background:`linear-gradient(135deg,${C.primary},${C.secondary})`,border:"none",borderRadius:"50%",width:44,height:44,display:"flex",alignItems:"center",justifyContent:"center",cursor:"pointer",flexShrink:0,boxShadow:`0 4px 14px ${C.primary}50`,marginBottom:2}}>
                <Ic n="send" col="#fff" sz={18}/>
              </button>
            ):(
              <button
                onMouseDown={()=>setRec(true)}
                onMouseUp={()=>{if(recSecs<1)setRec(false);}}
                onTouchStart={()=>setRec(true)}
                onTouchEnd={()=>{if(recSecs<1)setRec(false);}}
                style={{background:`linear-gradient(135deg,${C.primary},${C.secondary})`,border:"none",borderRadius:"50%",width:44,height:44,display:"flex",alignItems:"center",justifyContent:"center",cursor:"pointer",flexShrink:0,boxShadow:`0 4px 14px ${C.primary}50`,marginBottom:2}}>
                <Ic n="mic" col="#fff" sz={20}/>
              </button>
            )}
          </div>
        )}
      </div>
    );
  }

  // Add by phone modal
  const AddPhoneModal = () => (
    <div style={{position:"fixed",inset:0,background:"rgba(0,0,0,0.85)",zIndex:300,display:"flex",alignItems:"flex-end",justifyContent:"center"}}
      onClick={()=>{setShowAddPhone(false);setPhoneInput("");setPhoneResult(null);setPhoneSearched(false);}}>
      <div onClick={e=>e.stopPropagation()} style={{width:"100%",maxWidth:430,background:C.card,borderRadius:"24px 24px 0 0",padding:"24px 20px 40px"}}>
        <div style={{width:40,height:4,background:C.border,borderRadius:2,margin:"0 auto 20px"}}/>
        <div style={{color:C.text,fontWeight:800,fontSize:18,marginBottom:6,fontFamily:"'Bebas Neue',sans-serif",letterSpacing:1}}>Add Friend by Phone Number</div>
        <div style={{color:C.muted,fontSize:13,marginBottom:20}}>Enter their South African number to find them on VIVID</div>
        <div style={{display:"flex",gap:10,marginBottom:16}}>
          <div style={{background:C.surface,border:`1px solid ${C.border}`,borderRadius:14,padding:"12px 16px",display:"flex",alignItems:"center",gap:10,flex:1}}>
            <span style={{fontSize:18}}>🇿🇦</span>
            <input
              value={phoneInput}
              onChange={e=>setPhoneInput(e.target.value)}
              onKeyDown={e=>e.key==="Enter"&&searchByPhone()}
              placeholder="+27 74 857 5764"
              style={{flex:1,background:"none",border:"none",color:C.text,fontSize:15,outline:"none",fontFamily:"'DM Sans',sans-serif"}}
            />
          </div>
          <button onClick={searchByPhone} style={{background:`linear-gradient(135deg,${C.primary},${C.secondary})`,border:"none",borderRadius:14,padding:"12px 18px",color:"#fff",fontWeight:700,cursor:"pointer",fontSize:14}}>
            Find
          </button>
        </div>
        {phoneSearched&&(
          phoneResult?(
            <div style={{background:C.surface,borderRadius:16,padding:"14px 16px",display:"flex",alignItems:"center",gap:12}}>
              <Av user={phoneResult} size={50}/>
              <div style={{flex:1}}>
                <div style={{color:C.text,fontWeight:700,fontSize:15}}>{phoneResult.name}</div>
                <div style={{color:C.muted,fontSize:12}}>{phoneResult.handle} · {phoneResult.followers} followers</div>
              </div>
              <button onClick={()=>setFollowed(f=>({...f,[phoneResult.id]:!f[phoneResult.id]}))} style={{background:followed[phoneResult.id]?C.surface2:`linear-gradient(135deg,${C.primary},${C.secondary})`,border:followed[phoneResult.id]?`1px solid ${C.border}`:"none",borderRadius:12,padding:"8px 14px",color:C.text,fontWeight:700,cursor:"pointer",fontSize:13}}>
                {followed[phoneResult.id]?"Following":"Follow"}
              </button>
            </div>
          ):(
            <div style={{textAlign:"center",padding:"16px 0"}}>
              <div style={{fontSize:36,marginBottom:8}}>🔍</div>
              <div style={{color:C.muted,fontSize:14}}>No user found with that number</div>
              <div style={{color:C.muted,fontSize:12,marginTop:4}}>Try: +27 82 111 2233</div>
            </div>
          )
        )}
      </div>
    </div>
  );

  const onlineFriends = USERS.filter(u => u.id !== ME.id && [1,2].includes(u.id));
  const NAV=[
    {id:"messages", icon:"msg",  label:"Chats",   badge:totalUnread},
    {id:"home",     icon:"home", label:"Feed",    badge:0},
    {id:"create",   icon:null,   label:"",        badge:0},
    {id:"reels",    icon:"reel", label:"Reels",   badge:0},
    {id:"profile",  icon:"user", label:"Me",      badge:0},
  ];

  return(
    <div style={{width:"100%",maxWidth:430,margin:"0 auto",height:"100vh",background:C.bg,display:"flex",flexDirection:"column",fontFamily:"'DM Sans',sans-serif",overflow:"hidden",position:"relative"}}>
      <style>{`
        @import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=DM+Sans:wght@400;500;700;800&display=swap');
        *{box-sizing:border-box;margin:0;padding:0}
        ::-webkit-scrollbar{width:0}
        textarea::placeholder,input::placeholder{color:#7b7b9a}
        @keyframes heartpop{0%{transform:scale(1)}50%{transform:scale(1.4)}100%{transform:scale(1)}}
      `}</style>

      {showAddPhone && <AddPhoneModal/>}

      {/* ── MESSAGES (default tab) ── */}
      {tab==="messages"&&!openChat&&(
        <div style={{flex:1,display:"flex",flexDirection:"column",overflow:"hidden"}}>
          {/* Header */}
          <div style={{padding:"16px 18px 10px",background:C.bg,borderBottom:`1px solid ${C.border}`,flexShrink:0}}>
            <div style={{display:"flex",alignItems:"center",justifyContent:"space-between",marginBottom:14}}>
              <div style={{fontFamily:"'Bebas Neue',sans-serif",fontSize:28,letterSpacing:2,background:`linear-gradient(135deg,${C.primary},${C.accent})`,WebkitBackgroundClip:"text",WebkitTextFillColor:"transparent"}}>VIVID</div>
              <div style={{display:"flex",gap:10,alignItems:"center"}}>
                <button onClick={()=>setShowAddPhone(true)} style={{background:`${C.primary}22`,border:`1px solid ${C.primary}44`,borderRadius:20,padding:"6px 12px",color:C.primary,fontSize:12,fontWeight:700,cursor:"pointer",display:"flex",alignItems:"center",gap:5}}>
                  <Ic n="adduser" col={C.primary} sz={14}/>
                  Add
                </button>
                <button style={{background:"none",border:"none",cursor:"pointer"}}><Ic n="srch" col={C.muted} sz={22}/></button>
              </div>
            </div>
            {/* Search */}
            <div style={{background:C.surface,borderRadius:14,padding:"9px 14px",display:"flex",alignItems:"center",gap:8,marginBottom:12}}>
              <Ic n="srch" col={C.muted} sz={16}/>
              <input value={search} onChange={e=>setSearch(e.target.value)} placeholder="Search messages..." style={{flex:1,background:"none",border:"none",color:C.text,fontSize:14,outline:"none",fontFamily:"'DM Sans',sans-serif"}}/>
            </div>
            {/* Tabs */}
            <div style={{display:"flex",gap:6}}>
              {[["all","All"],["unread","Unread"],["groups","Groups"]].map(([k,l])=>(
                <button key={k} onClick={()=>setChatTab(k)} style={{background:chatTab===k?C.primary:C.surface,border:"none",borderRadius:20,padding:"6px 14px",color:chatTab===k?"#fff":C.muted,fontWeight:700,fontSize:12,cursor:"pointer",transition:"all 0.2s"}}>
                  {l}{k==="unread"&&totalUnread>0?` (${totalUnread})`:""}
                </button>
              ))}
            </div>
          </div>
          {/* Chat list */}
          <div style={{flex:1,overflowY:"auto"}}>
            {filtered.length===0?(
              <div style={{textAlign:"center",padding:"40px 20px"}}>
                <div style={{fontSize:40,marginBottom:10}}>💬</div>
                <div style={{color:C.muted,fontSize:14}}>No chats found</div>
              </div>
            ):filtered.map(chat=><ChatRow key={chat.id} chat={chat} onOpen={openChatFn}/>)}
          </div>
        </div>
      )}

      {/* ── HOME / FEED ── */}
      {tab==="home"&&(
        <div style={{flex:1,overflowY:"auto",paddingBottom:72}}>
          <div style={{padding:"16px 18px 10px",display:"flex",alignItems:"center",justifyContent:"space-between",background:C.bg,borderBottom:`1px solid ${C.border}`,position:"sticky",top:0,zIndex:10}}>
            <div style={{fontFamily:"'Bebas Neue',sans-serif",fontSize:28,letterSpacing:2,background:`linear-gradient(135deg,${C.primary},${C.accent})`,WebkitBackgroundClip:"text",WebkitTextFillColor:"transparent"}}>VIVID</div>
            <div style={{fontSize:13,color:C.muted,fontWeight:600}}>🇿🇦 East Rand</div>
          </div>
          {/* Stories */}
          <div style={{padding:"14px 0 14px 16px",display:"flex",gap:14,overflowX:"auto"}}>
            <div style={{display:"flex",flexDirection:"column",alignItems:"center",gap:6,flexShrink:0,cursor:"pointer"}}>
              <div style={{width:62,height:62,borderRadius:"50%",border:`2px dashed ${C.primary}`,display:"flex",alignItems:"center",justifyContent:"center",background:C.surface}}><span style={{color:C.primary,fontSize:22}}>+</span></div>
              <span style={{color:C.muted,fontSize:11}}>Your story</span>
            </div>
            {STORIES.map((s,i)=>(
              <div key={s.id} onClick={()=>setOpenStory(i)} style={{display:"flex",flexDirection:"column",alignItems:"center",gap:6,flexShrink:0,cursor:"pointer"}}>
                <Av user={s.user} size={62} border={!s.seen}/>
                <span style={{color:s.seen?C.muted:C.text,fontSize:11,maxWidth:62,textAlign:"center",overflow:"hidden",textOverflow:"ellipsis",whiteSpace:"nowrap"}}>{s.user.name.split(" ")[0]}</span>
              </div>
            ))}
          </div>
          {/* Feed */}
          {posts.map(post=>(
            <div key={post.id} style={{background:C.card,borderBottom:`1px solid ${C.border}`}}>
              <div style={{padding:"13px 16px",display:"flex",alignItems:"center",gap:10}}>
                <div onClick={()=>setViewProf(post.user.id)} style={{cursor:"pointer"}}><Av user={post.user} size={42}/></div>
                <div style={{flex:1}}>
                  <div onClick={()=>setViewProf(post.user.id)} style={{cursor:"pointer",display:"flex",alignItems:"center",gap:5}}>
                    <span style={{color:C.text,fontWeight:700,fontSize:14}}>{post.user.name}</span>
                    {post.user.verified&&<Ic n="vfy"/>}
                  </div>
                  <div style={{color:C.muted,fontSize:11}}>{post.time}</div>
                </div>
                <Ic n="more" col={C.muted} sz={20}/>
              </div>
              <div style={{height:260,background:post.gradient,display:"flex",alignItems:"center",justifyContent:"center",fontSize:72}}>{post.emoji}</div>
              <div style={{padding:"12px 16px"}}>
                <div style={{color:C.text,fontSize:14,lineHeight:1.5,marginBottom:12}}>{post.content}</div>
                <div style={{display:"flex",gap:20}}>
                  {[["heart",post.liked,()=>setPosts(p=>p.map(x=>x.id===post.id?{...x,liked:!x.liked,likes:x.liked?x.likes-1:x.likes+1}:x)),fN(post.likes)],
                    ["cmnt",false,null,fN(post.comments)],
                    ["shr",false,null,fN(post.shares)]].map(([ic,act,fn,val])=>(
                    <button key={ic} onClick={fn||undefined} style={{background:"none",border:"none",cursor:fn?"pointer":"default",display:"flex",alignItems:"center",gap:6}}>
                      <Ic n={ic} active={act} sz={22}/>
                      <span style={{color:act?C.primary:C.muted,fontSize:13,fontWeight:600}}>{val}</span>
                    </button>
                  ))}
                </div>
              </div>
            </div>
          ))}
        </div>
      )}

      {/* ── REELS (TikTok/Instagram style) ── */}
      {tab==="reels"&&(
        <div style={{flex:1,position:"relative",overflow:"hidden"}}>
          {/* Full-screen reel */}
          {REELS.map((r,i)=>(
            <div key={r.id} style={{position:"absolute",inset:0,background:r.bg,display:activeReel===i?"flex":"none",flexDirection:"column",justifyContent:"flex-end",transition:"opacity 0.3s"}}>
              {/* Big emoji bg */}
              <div style={{position:"absolute",inset:0,display:"flex",alignItems:"center",justifyContent:"center",fontSize:120,opacity:0.12,pointerEvents:"none"}}>{r.emoji}</div>

              {/* Play button */}
              <div style={{position:"absolute",inset:0,display:"flex",alignItems:"center",justifyContent:"center",pointerEvents:"none"}}>
                <div style={{background:"rgba(255,255,255,0.15)",borderRadius:"50%",width:72,height:72,display:"flex",alignItems:"center",justifyContent:"center",backdropFilter:"blur(12px)",fontSize:30}}>▶</div>
              </div>

              {/* Audio ticker */}
              <div style={{position:"absolute",top:60,left:16,right:80,display:"flex",alignItems:"center",gap:8}}>
                <div style={{background:"rgba(0,0,0,0.4)",borderRadius:20,padding:"5px 12px",backdropFilter:"blur(8px)",display:"flex",alignItems:"center",gap:6,overflow:"hidden",flex:1}}>
                  <span style={{fontSize:13,flexShrink:0}}>🎵</span>
                  <span style={{color:"#fff",fontSize:12,fontWeight:600,whiteSpace:"nowrap",overflow:"hidden",textOverflow:"ellipsis"}}>{r.audio.replace("🎵 ","")}</span>
                </div>
              </div>

              {/* Bottom info */}
              <div style={{padding:"0 72px 100px 16px",background:"linear-gradient(0deg,rgba(0,0,0,0.7) 0%,transparent 100%)"}}>
                <div onClick={()=>setViewProf(r.user.id)} style={{display:"flex",alignItems:"center",gap:10,marginBottom:10,cursor:"pointer"}}>
                  <Av user={r.user} size={42} border/>
                  <div>
                    <div style={{color:"#fff",fontWeight:700,fontSize:15}}>{r.user.name}</div>
                    <div style={{color:"rgba(255,255,255,0.7)",fontSize:12}}>{r.user.handle}</div>
                  </div>
                  <button onClick={e=>{e.stopPropagation();setFollowed(f=>({...f,[r.user.id]:!f[r.user.id]}));}} style={{marginLeft:8,background:followed[r.user.id]?"rgba(255,255,255,0.15)":`linear-gradient(135deg,${C.primary},${C.secondary})`,border:followed[r.user.id]?"1px solid rgba(255,255,255,0.4)":"none",borderRadius:20,padding:"5px 14px",color:"#fff",fontWeight:700,cursor:"pointer",fontSize:12}}>
                    {followed[r.user.id]?"Following":"Follow"}
                  </button>
                </div>
                <div style={{color:"rgba(255,255,255,0.92)",fontSize:14,marginBottom:8,lineHeight:1.4}}>{r.caption}</div>
                <div style={{display:"flex",gap:10,flexWrap:"wrap"}}>
                  {r.tags.map(t=><span key={t} style={{color:C.accent,fontSize:12,fontWeight:600}}>{t}</span>)}
                </div>
              </div>

              {/* Right action bar */}
              <div style={{position:"absolute",right:12,bottom:110,display:"flex",flexDirection:"column",gap:22,alignItems:"center"}}>
                {/* Like */}
                <div style={{display:"flex",flexDirection:"column",alignItems:"center",gap:4}}>
                  <button onClick={()=>setReelLiked(l=>({...l,[r.id]:!l[r.id]}))} style={{width:46,height:46,borderRadius:"50%",background:"rgba(0,0,0,0.3)",backdropFilter:"blur(10px)",border:"none",display:"flex",alignItems:"center",justifyContent:"center",cursor:"pointer",fontSize:22,animation:reelLiked[r.id]?"heartpop 0.3s ease":undefined}}>
                    {reelLiked[r.id]?"❤️":"🤍"}
                  </button>
                  <span style={{color:"#fff",fontSize:11,fontWeight:700}}>{reelLiked[r.id]?fN(parseInt(r.likes.replace("K",""))*1000+1):r.likes}</span>
                </div>
                {/* Comment */}
                <div style={{display:"flex",flexDirection:"column",alignItems:"center",gap:4}}>
                  <div style={{width:46,height:46,borderRadius:"50%",background:"rgba(0,0,0,0.3)",backdropFilter:"blur(10px)",display:"flex",alignItems:"center",justifyContent:"center",cursor:"pointer",fontSize:22}}>💬</div>
                  <span style={{color:"#fff",fontSize:11,fontWeight:700}}>{r.comments}</span>
                </div>
                {/* Share */}
                <div style={{display:"flex",flexDirection:"column",alignItems:"center",gap:4}}>
                  <div style={{width:46,height:46,borderRadius:"50%",background:"rgba(0,0,0,0.3)",backdropFilter:"blur(10px)",display:"flex",alignItems:"center",justifyContent:"center",cursor:"pointer",fontSize:22}}>➦</div>
                  <span style={{color:"#fff",fontSize:11,fontWeight:700}}>{r.shares}</span>
                </div>
                {/* Save */}
                <div style={{display:"flex",flexDirection:"column",alignItems:"center",gap:4}}>
                  <button onClick={()=>setReelSaved(s=>({...s,[r.id]:!s[r.id]}))} style={{width:46,height:46,borderRadius:"50%",background:"rgba(0,0,0,0.3)",backdropFilter:"blur(10px)",border:"none",display:"flex",alignItems:"center",justifyContent:"center",cursor:"pointer",fontSize:22}}>
                    {reelSaved[r.id]?"🔖":"📌"}
                  </button>
                  <span style={{color:"#fff",fontSize:11,fontWeight:700}}>{r.saves}</span>
                </div>
                {/* Creator avatar */}
                <div style={{marginTop:4}}>
                  <div style={{width:46,height:46,borderRadius:"50%",border:`2px solid #fff`,overflow:"hidden",cursor:"pointer"}} onClick={()=>setViewProf(r.user.id)}>
                    <Av user={r.user} size={46}/>
                  </div>
                </div>
              </div>

              {/* Scroll nav dots */}
              <div style={{position:"absolute",right:64,top:"50%",transform:"translateY(-50%)",display:"flex",flexDirection:"column",gap:6}}>
                {REELS.map((_,j)=>(
                  <div key={j} onClick={()=>setActiveReel(j)} style={{width:4,height:activeReel===j?20:4,borderRadius:2,background:activeReel===j?"#fff":"rgba(255,255,255,0.4)",cursor:"pointer",transition:"height 0.2s"}}/>
                ))}
              </div>

              {/* Swipe hint arrows */}
              <div style={{position:"absolute",left:"50%",transform:"translateX(-50%)",bottom:90,display:"flex",flexDirection:"column",alignItems:"center",gap:4,opacity:0.5}}>
                {i>0&&<button onClick={()=>setActiveReel(i-1)} style={{background:"none",border:"none",color:"#fff",cursor:"pointer",fontSize:20,lineHeight:1}}>↑</button>}
                {i<REELS.length-1&&<button onClick={()=>setActiveReel(i+1)} style={{background:"none",border:"none",color:"#fff",cursor:"pointer",fontSize:20,lineHeight:1}}>↓</button>}
              </div>
            </div>
          ))}

          {/* Add friend via phone - floating button on reels */}
          <button onClick={()=>setShowAddPhone(true)} style={{position:"absolute",top:16,right:16,background:"rgba(0,0,0,0.5)",backdropFilter:"blur(10px)",border:`1px solid rgba(255,255,255,0.2)`,borderRadius:20,padding:"7px 14px",color:"#fff",fontSize:12,fontWeight:700,cursor:"pointer",display:"flex",alignItems:"center",gap:6,zIndex:20}}>
            <Ic n="adduser" col="#fff" sz={14}/>
            Add Friend
          </button>
        </div>
      )}

      {/* ── PROFILE ── */}
      {tab==="profile"&&(
        <div style={{flex:1,overflowY:"auto",paddingBottom:72}}>
          <div style={{background:`linear-gradient(180deg,${ME.color}55 0%,transparent 100%)`,padding:"30px 20px 20px",textAlign:"center"}}>
            <Av user={ME} size={90} border/>
            <div style={{marginTop:14,color:C.text,fontWeight:800,fontSize:22,fontFamily:"'Bebas Neue',sans-serif",letterSpacing:1.5}}>{ME.name}</div>
            <div style={{color:C.muted,fontSize:13,marginBottom:6}}>{ME.handle}</div>
            <div style={{color:C.text,fontSize:14,marginBottom:20}}>{ME.bio}</div>
            <div style={{display:"flex",justifyContent:"center",gap:28,marginBottom:20}}>
              {[["Posts",ME.posts],["Followers",ME.followers],["Following",ME.following]].map(([l,v])=>(
                <div key={l}><div style={{color:C.text,fontWeight:800,fontSize:20,fontFamily:"'Bebas Neue',sans-serif"}}>{v}</div><div style={{color:C.muted,fontSize:12}}>{l}</div></div>
              ))}
            </div>
            <button style={{background:C.surface,border:`1px solid ${C.border}`,borderRadius:12,padding:"10px 32px",color:C.text,fontWeight:700,cursor:"pointer",fontSize:14}}>Edit Profile</button>
          </div>
          {/* People you may know */}
          <div style={{padding:"16px 20px"}}>
            <div style={{color:C.text,fontWeight:700,fontSize:15,marginBottom:12}}>People you may know</div>
            <div style={{display:"flex",flexDirection:"column",gap:12}}>
              {USERS.filter(u=>u.id!==ME.id).map(user=>(
                <div key={user.id} style={{display:"flex",alignItems:"center",gap:12,background:C.card,borderRadius:16,padding:"12px 14px"}}>
                  <div onClick={()=>setViewProf(user.id)} style={{cursor:"pointer"}}><Av user={user} size={46}/></div>
                  <div style={{flex:1}}>
                    <div onClick={()=>setViewProf(user.id)} style={{cursor:"pointer",display:"flex",alignItems:"center",gap:5}}>
                      <span style={{color:C.text,fontWeight:700,fontSize:14}}>{user.name}</span>
                      {user.verified&&<Ic n="vfy"/>}
                    </div>
                    <div style={{color:C.muted,fontSize:12}}>{user.followers} followers</div>
                  </div>
                  <button onClick={()=>setFollowed(f=>({...f,[user.id]:!f[user.id]}))} style={{background:followed[user.id]?C.surface:`linear-gradient(135deg,${C.primary},${C.secondary})`,border:followed[user.id]?`1px solid ${C.border}`:"none",borderRadius:10,padding:"7px 14px",color:C.text,fontWeight:700,cursor:"pointer",fontSize:12}}>
                    {followed[user.id]?"Following":"Follow"}
                  </button>
                </div>
              ))}
            </div>
          </div>
        </div>
      )}

      {/* ── CREATE ── */}
      {tab==="create"&&(
        <div style={{flex:1,background:C.bg,display:"flex",flexDirection:"column",alignItems:"center",justifyContent:"center",gap:24,paddingBottom:72}}>
          <div style={{fontFamily:"'Bebas Neue',sans-serif",fontSize:30,letterSpacing:3,color:C.text}}>CREATE</div>
          <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:14,width:"100%",maxWidth:340,padding:"0 20px"}}>
            {[
              {icon:"🎬",label:"Record Video",desc:"Shoot up to 3 min",grad:`linear-gradient(135deg,${C.primary},#ff6b35)`},
              {icon:"📤",label:"Upload Video",desc:"From your gallery",grad:`linear-gradient(135deg,${C.secondary},#00e5ff)`},
              {icon:"✨",label:"Add Effects",desc:"Filters & stickers",grad:`linear-gradient(135deg,#ffd600,${C.primary})`},
              {icon:"🎵",label:"Add Sound",desc:"Trending audio",grad:`linear-gradient(135deg,#00e5ff,${C.secondary})`},
            ].map(opt=>(
              <div key={opt.label} style={{background:C.card,borderRadius:20,padding:"22px 16px",display:"flex",flexDirection:"column",alignItems:"center",gap:10,cursor:"pointer",border:`1px solid ${C.border}`}}>
                <div style={{width:52,height:52,borderRadius:16,background:opt.grad,display:"flex",alignItems:"center",justifyContent:"center",fontSize:26}}>{opt.icon}</div>
                <div style={{color:C.text,fontWeight:700,fontSize:13,textAlign:"center"}}>{opt.label}</div>
                <div style={{color:C.muted,fontSize:11,textAlign:"center"}}>{opt.desc}</div>
              </div>
            ))}
          </div>
          <button onClick={()=>setTab("messages")} style={{background:"none",border:`1px solid ${C.border}`,borderRadius:20,padding:"10px 28px",color:C.muted,fontSize:13,cursor:"pointer"}}>Cancel</button>
        </div>
      )}

      {/* ── BOTTOM NAV ── */}
      <div style={{position:"absolute",bottom:0,left:0,right:0,background:tab==="reels"?"transparent":C.card,borderTop:tab==="reels"?"none":`1px solid ${C.border}20`,display:"flex",alignItems:"center",height:72,zIndex:20,backdropFilter:"blur(20px)"}}>
        {NAV.map(n=>(
          <button key={n.id} onClick={()=>{setTab(n.id);setOpenChat(null);}} style={{flex:1,background:"none",border:"none",cursor:"pointer",display:"flex",flexDirection:"column",alignItems:"center",justifyContent:"center",gap:4,height:"100%",position:"relative"}}>
            {n.id==="create"?(
              <div style={{position:"relative",width:52,height:34}}>
                <div style={{position:"absolute",left:0,top:0,width:40,height:34,borderRadius:10,background:C.accent,opacity:0.9}}/>
                <div style={{position:"absolute",right:0,top:0,width:40,height:34,borderRadius:10,background:C.primary,opacity:0.9}}/>
                <div style={{position:"absolute",left:"50%",top:"50%",transform:"translate(-50%,-50%)",width:34,height:28,borderRadius:8,background:C.card,display:"flex",alignItems:"center",justifyContent:"center"}}>
                  <Ic n="cam" col={C.text} sz={17}/>
                </div>
              </div>
            ):(
              <>
                <div style={{position:"relative"}}>
                  <Ic n={n.icon} active={tab===n.id} sz={26}/>
                  {n.badge>0&&(
                    <div style={{position:"absolute",top:-4,right:-7,background:C.online,borderRadius:10,minWidth:16,height:16,display:"flex",alignItems:"center",justifyContent:"center",fontSize:9,fontWeight:800,color:"#fff",border:`2px solid ${tab==="reels"?"transparent":C.card}`,padding:"0 3px"}}>
                      {n.badge}
                    </div>
                  )}
                </div>
                <span style={{color:tab===n.id?C.primary:tab==="reels"?"rgba(255,255,255,0.7)":C.muted,fontSize:10,fontWeight:700,letterSpacing:0.3}}>{n.label}</span>
              </>
            )}
          </button>
        ))}
      </div>
    </div>
  );
}
