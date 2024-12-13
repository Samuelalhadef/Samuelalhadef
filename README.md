import React from 'react';
import { FaGithub, FaLinkedin, FaEnvelope, FaCode, FaLanguage, FaGraduationCap } from 'lucide-react';

const GitHubProfile = () => {
  const skills = [
    'Python', 'JavaScript', 'HTML', 'CSS', 'PHP',
    'Front-end Development', 'Back-end Development', 'Project Management'
  ];

  const languages = [
    { name: 'French', level: 'Native' },
    { name: 'English', level: 'B2 (TOEFL)' },
    { name: 'Spanish', level: 'A2' },
    { name: 'Russian', level: 'A2' }
  ];

  return (
    <div className="min-h-screen bg-[#F5E6D3] text-[#2C3E50] font-serif">
      {/* Renaissance-inspired Header */}
      <div className="relative h-[400px] overflow-hidden">
        <svg 
          viewBox="0 0 1440 400" 
          className="absolute inset-0 w-full h-full"
          preserveAspectRatio="xMidYMid slice"
        >
          <defs>
            <linearGradient id="renaissance-gradient" x1="0%" y1="0%" x2="100%" y2="100%">
              <stop offset="0%" stopColor="#B76D68" stopOpacity="0.6"/>
              <stop offset="100%" stopColor="#4A7C59" stopOpacity="0.6"/>
            </linearGradient>
          </defs>
          <path 
            d="M0,160 Q720,320 1440,160 L1440,400 L0,400 Z" 
            fill="url(#renaissance-gradient)"
          />
        </svg>
        <div className="absolute inset-0 flex items-center justify-center text-center">
          <div>
            <h1 className="text-5xl font-bold text-white drop-shadow-lg">Samuel Alhadef</h1>
            <p className="text-xl text-white mt-4 drop-shadow-md">
              Web Development Student | Innovative Digital Creator
            </p>
          </div>
        </div>
      </div>

      {/* Main Content */}
      <div className="container mx-auto px-6 py-12">
        <div className="grid md:grid-cols-3 gap-8">
          {/* Profile Section */}
          <div className="bg-white p-6 rounded-lg shadow-lg">
            <h2 className="text-2xl font-semibold border-b-2 border-[#4A7C59] pb-2 mb-4">
              <FaCode className="inline-block mr-2" /> Professional Profile
            </h2>
            <p className="text-[#2C3E50]">
              Passionate web development student with hands-on experience in coding, 
              front-end and back-end programming, and project management. Skilled in 
              HTML, CSS, JavaScript, and Python, driven to create innovative web solutions 
              and contribute to team success.
            </p>
          </div>

          {/* Skills Section */}
          <div className="bg-white p-6 rounded-lg shadow-lg">
            <h2 className="text-2xl font-semibold border-b-2 border-[#4A7C59] pb-2 mb-4">
              <FaGraduationCap className="inline-block mr-2" /> Technical Skills
            </h2>
            <div className="flex flex-wrap gap-2">
              {skills.map((skill, index) => (
                <span 
                  key={index} 
                  className="bg-[#B76D68] text-white px-3 py-1 rounded-full text-sm"
                >
                  {skill}
                </span>
              ))}
            </div>
          </div>

          {/* Languages Section */}
          <div className="bg-white p-6 rounded-lg shadow-lg">
            <h2 className="text-2xl font-semibold border-b-2 border-[#4A7C59] pb-2 mb-4">
              <FaLanguage className="inline-block mr-2" /> Languages
            </h2>
            {languages.map((lang, index) => (
              <div key={index} className="flex justify-between mb-2">
                <span>{lang.name}</span>
                <span className="text-[#4A7C59]">{lang.level}</span>
              </div>
            ))}
          </div>
        </div>

        {/* Contact & Social */}
        <div className="mt-8 flex justify-center space-x-6">
          <a 
            href="mailto:samuel.alhadef@gmail.com" 
            className="text-[#2C3E50] hover:text-[#B76D68] transition-colors"
          >
            <FaEnvelope size={32} />
          </a>
          <a 
            href="https://linkedin.com/in/samuel-alhadef" 
            target="_blank" 
            rel="noopener noreferrer"
            className="text-[#2C3E50] hover:text-[#B76D68] transition-colors"
          >
            <FaLinkedin size={32} />
          </a>
          <a 
            href="https://github.com/samuelalhadef" 
            target="_blank" 
            rel="noopener noreferrer"
            className="text-[#2C3E50] hover:text-[#B76D68] transition-colors"
          >
            <FaGithub size={32} />
          </a>
        </div>
      </div>
    </div>
  );
};

export default GitHubProfile;
