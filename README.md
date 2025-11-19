# DevSecOps Pipeline Implementation for Tic Tac Toe Game

![Screenshot 2025-03-04 at 7 16 48 PM](https://github.com/user-attachments/assets/7ed79f9c-9144-4870-accd-500085a15592)

![image](https://github.com/user-attachments/assets/5b2813a5-f493-4665-8964-77359b5be93a)

## Features

- 🎮 Fully functional Tic Tac Toe game
- 📊 Score tracking for X, O, and draws
- 📜 Game history with timestamps
- 🏆 Highlights winning combinations
- 🔄 Reset game and statistics
- 📱 Responsive design for all devices

## Technologies Used

- React 18
- TypeScript
- Tailwind CSS
- Lucide React for icons

## Project Structure

```
src/
├── components/
│   ├── Board.tsx       # Game board component
│   ├── Square.tsx      # Individual square component
│   ├── ScoreBoard.tsx  # Score tracking component
│   └── GameHistory.tsx # Game history component
├── utils/
│   └── gameLogic.ts    # Game logic utilities
├── App.tsx             # Main application component
└── main.tsx           # Entry point
```

## Game Logic

The game implements the following rules:

1. X goes first, followed by O
2. The first player to get 3 of their marks in a row (horizontally, vertically, or diagonally) wins
3. If all 9 squares are filled and no player has 3 marks in a row, the game is a draw
4. Winning combinations are highlighted
5. Game statistics are tracked and displayed

## Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/devsecops-demo.git
   cd devsecops-demo
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn
   ```

3. Start the development server:
   ```bash
   npm run dev
   # or
   yarn dev
   ```

4. Open your browser and navigate to `http://localhost:5173`

## Building for Production

To create a production build:

```bash
npm run build
# or
yarn build
```

The build artifacts will be stored in the `dist/` directory.
+     67: 
+     68: ## 🛡️ Security Features
+     69: 
+     70: ### **Multi-Layer Security**
+     71: - **SAST Scanning**: CodeQL + ESLint security analysis
+     72: - **Container Scanning**: Trivy + Snyk vulnerability detection
+     73: - **Image Signing**: Cosign keyless signing for supply chain security
+     74: - **SBOM Generation**: Complete software bill of materials
+     75: - **Private Registry**: GitHub Container Registry with access controls
+     76: 
+     77: ### **Security Layers**
+     78: ```
+     79: 🛡️ SECURITY STACK:
+     80: ├── Code Analysis (SAST)
+     81: ├── Dependency Scanning  
+     82: ├── Container Scanning
+     83: ├── Image Signing
+     84: ├── SBOM Generation
+     85: ├── Runtime Protection
+     86: └── Compliance Monitoring
+     87: ```
+     88: 
+     89: ## 🚀 Pipeline Stages
+     90: 
+     91: ### **1. Unit Tests**
+     92: - ✅ Jest test runner with coverage
+     93: - 📊 Coverage reports uploaded
+     94: - 🚫 Pipeline fails if tests fail
+     95: 
+     96: ### **2. Static Code Analysis (SAST)**
+     97: - 🔍 GitHub CodeQL for security vulnerabilities
+     98: - 🛡️ ESLint security rules
+     99: - 📊 Results uploaded to Security tab
+    100: 
+    101: ### **3. Build Application**
+    102: - ⚛️ React application build
+    103: - 📦 Vite bundler optimization
+    104: - 🏗️ Build artifacts stored
+    105: 
+    106: ### **4. Docker Security Pipeline**
+    107: - 🐳 Multi-stage Docker build
+    108: - 🔍 Trivy vulnerability scanning
+    109: - 🛡️ Snyk container security scan
+    110: - 📋 SBOM generation with Anchore
+    111: - ✍️ Image signing with Cosign
+    112: - 📤 Push to GitHub Container Registry
+    113: 
+    114: ### **5. GitOps Integration**
+    115: - 📝 Automatic image tag updates
+    116: - 🔄 ArgoCD change detection
+    117: - 🚀 Kubernetes deployment
+    118: 
+    119: ## 📦 Container Registry
+    120: 
+    121: **Location**: `ghcr.io/agatha-r3/devsecops-argocd`
+    122: 
+    123: ### **Image Tags**
+    124: ```bash
+    125: # Latest stable
+    126: ghcr.io/agatha-r3/devsecops-argocd:latest
+    127: 
+    128: # Branch-specific
+    129: ghcr.io/agatha-r3/devsecops-argocd:main-<commit-sha>
+    130: 
+    131: # Pull request
+    132: ghcr.io/agatha-r3/devsecops-argocd:pr-<number>
+    133: ```
+    134: 
+    135: ### **Security Verification**
+    136: ```bash
+    137: # Verify image signature
+    138: cosign verify ghcr.io/agatha-r3/devsecops-argocd:latest
+    139: 
+    140: # Download SBOM
+    141: cosign download sbom ghcr.io/agatha-r3/devsecops-argocd:latest
+    142: 
+    143: # View attestations
+    144: cosign download attestation ghcr.io/agatha-r3/devsecops-argocd:latest
+    145: ```
+    146: 
+    147: ## ⚙️ Setup Instructions
+    148: 
+    149: ### **1. Repository Setup**
+    150: ```bash
+    151: # Clone repository
+    152: git clone https://github.com/Agatha-r3/DevSecOps-argoCD.git
+    153: cd DevSecOps-argoCD
+    154: 
+    155: # Install dependencies
+    156: npm install
+    157: 
+    158: # Run locally
+    159: npm run dev
+    160: ```
+    161: 
+    162: ### **2. Required Secrets**
+    163: Add these secrets in GitHub Settings > Secrets and variables > Actions:
+    164: 
+    165: ```bash
+    166: SNYK_TOKEN          # Snyk API token (optional)
+    167: GITOPS_TOKEN        # GitHub PAT for GitOps repo access
+    168: ARGOCD_SERVER       # ArgoCD server URL (optional)
+    169: ARGOCD_TOKEN        # ArgoCD API token (optional)
+    170: ```
+    171: 
+    172: ### **3. GitOps Repository**
+    173: Create a separate repository for GitOps: `Agatha-r3/devsecops-argocd-gitops`
+    174: 
+    175: Structure:
+    176: ```
+    177: k8s/
+    178:   deployment.yaml
+    179:   service.yaml
+    180:   ingress.yaml
+    181: helm/
+    182:   values.yaml
+    183:   Chart.yaml
+    184: ```
+    185: 
+    186: ## 🔧 Troubleshooting
+    187: 
+    188: ### **Common Issues & Solutions**
+    189: 
+    190: #### **1. Pipeline Failures**
+    191: ```bash
+    192: # Check pipeline status
+    193: gh run list --repo Agatha-r3/DevSecOps-argoCD
+    194: 
+    195: # View detailed logs
+    196: gh run view --log
+    197: 
+    198: # Missing secrets
+    199: gh secret set SNYK_TOKEN --body "your-token"
+    200: ```
+    201: 
+    202: #### **2. Docker Build Issues**
+    203: ```bash
+    204: # Test build locally
+    205: docker build -t test-image .
+    206: 
+    207: # Check .dockerignore
+    208: echo "node_modules\n.git\n*.md" > .dockerignore
+    209: ```
+    210: 
+    211: #### **3. Security Scan Failures**
+    212: ```yaml
+    213: # Temporarily allow vulnerabilities
+    214: - name: Run Trivy
+    215:   continue-on-error: true
+    216: 
+    217: # Ignore specific issues
+    218: --ignore-unfixed --severity HIGH,CRITICAL
+    219: ```
+    220: 
+    221: #### **4. Permission Errors**
+    222: - Go to Settings > Actions > General
+    223: - Enable "Read and write permissions"
+    224: - Check token scopes: `write:packages`, `repo`
+    225: 
+    226: #### **5. Resource Optimization**
+    227: ```yaml
+    228: # Add caching
+    229: - uses: actions/cache@v3
+    230:   with:
+    231:     path: ~/.npm
+    232:     key: ${{ runner.os }}-node-${{ hashFiles('**/package-lock.json') }}
+    233: ```
+    234: 
+    235: ## 📊 Monitoring Pipeline
+    236: 
+    237: ### **GitHub Actions Dashboard**
+    238: - **Actions Tab**: View all pipeline runs
+    239: - **Security Tab**: Review vulnerability reports
+    240: - **Packages Tab**: See container images
+    241: - **Insights Tab**: Pipeline performance metrics
+    242: 
+    243: ### **Monitoring Commands**
+    244: ```bash
+    245: # List recent runs
+    246: gh run list
+    247: 
+    248: # Watch live run
+    249: gh run watch
+    250: 
+    251: # Download artifacts
+    252: gh run download <run-id>
+    253: 
+    254: # View security alerts
+    255: gh api repos/Agatha-r3/DevSecOps-argoCD/security-advisories
+    256: ```
+    257: 
+    258: ### **Pipeline Metrics**
+    259: - ⏱️ **Build Time**: ~5-8 minutes
+    260: - 🔍 **Security Scans**: Trivy + Snyk + CodeQL
+    261: - 📦 **Image Size**: ~50MB (optimized)
+    262: - ✅ **Success Rate**: Monitor in Actions tab
+    263: 
+    264: ## 🎯 Production Deployment
+    265: 
+    266: ### **ArgoCD Setup**
+    267: ```bash
+    268: # Install ArgoCD
+    269: kubectl create namespace argocd
+    270: kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
+    271: 
+    272: # Access ArgoCD UI
+    273: kubectl port-forward svc/argocd-server -n argocd 8080:443
+    274: ```
+    275: 
+    276: ### **Application Configuration**
+    277: ```yaml
+    278: apiVersion: argoproj.io/v1alpha1
+    279: kind: Application
+    280: metadata:
+    281:   name: devsecops-demo
+    282: spec:
+    283:   source:
+    284:     repoURL: https://github.com/Agatha-r3/devsecops-argocd-gitops
+    285:     path: k8s
+    286:   destination:
+    287:     server: https://kubernetes.default.svc
+    288:     namespace: default
+    289:   syncPolicy:
+    290:     automated:
+    291:       prune: true
+    292:       selfHeal: true
+    293: ```
+    294: 
+    295: ## 🔄 Continuous Feedback Loop
+    296: 
+    297: ```
+    298: 📊 Monitoring → 🚨 Alerts → 🔧 Fixes → 💻 Code → 🔄 Pipeline
+    299: ```
+    300: 
+    301: ### **Feedback Mechanisms**
+    302: - **GitHub Security Advisories**: Automated vulnerability alerts
+    303: - **Dependabot**: Dependency update PRs
+    304: - **Pipeline Notifications**: Slack/email integration
+    305: - **ArgoCD Sync Status**: Deployment health monitoring
+    306: 
+    307: ## 📈 Key Metrics
+    308: 
+    309: - **Security Coverage**: 100% code + container scanning
+    310: - **Build Automation**: Fully automated CI/CD
+    311: - **Deployment Speed**: GitOps-based continuous deployment
+    312: - **Supply Chain Security**: Signed images + SBOM tracking
+    313: - **Compliance**: Enterprise-grade security policies
+    314: 
+    315: ## 🏆 Best Practices Implemented
+    316: 
+    317: ✅ **Shift-Left Security**: Early vulnerability detection  
+    318: ✅ **Zero-Trust**: Verify all artifacts before deployment  
+    319: ✅ **GitOps**: Declarative, version-controlled deployments  
+    320: ✅ **Immutable Infrastructure**: Container-based deployments  
+    321: ✅ **Observability**: Comprehensive monitoring and logging  
+    322: ✅ **Compliance**: Automated security policy enforcement  
+    323: 
+    324: ## 🤝 Contributing
+    325: 
+    326: 1. Fork the repository
+    327: 2. Create feature branch: `git checkout -b feature/amazing-feature`
+    328: 3. Commit changes: `git commit -m 'Add amazing feature'`
+    329: 4. Push to branch: `git push origin feature/amazing-feature`
+    330: 5. Open Pull Request
+    331: 
+    332: ## 📄 License
+    333: 
+    334: This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
+    335: 
+    336: ## 🙏 Acknowledgments
+    337: 
+    338: - **GitHub Actions** for CI/CD platform
+    339: - **Trivy & Snyk** for security scanning
+    340: - **Cosign** for container signing
+    341: - **ArgoCD** for GitOps deployment
+    342: - **React & Vite** for application framework
+    343: 
+    344: ---


